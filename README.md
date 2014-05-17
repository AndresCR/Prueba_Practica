    boolean validar=true;
    int opcion;
    char continuar;
    double monto;

    Account oAccount=new Account();
    Scanner teclado=new Scanner(System.in);

    while (validar){
        System.out.println("Digite 1 si desea hacer un deposito o dogoye 2 si desea hacer un retiro"+"\n");
        opcion=Integer.parseInt(teclado.nextLine());
        {

        if(opcion==1){
            System.out.println("Digite el monto a depositar"+"\n");
            monto=Double.parseDouble(teclado.nextLine());
            oAccount.Deposito(monto);
        }
        if(opcion==2)
            System.out.println("Digite el monto a retirar"+"\n");
            monto=Double.parseDouble(teclado.nextLine());
            oAccount.Retiro(monto);
            if(oAccount.isHayError()){
                System.out.println("Elmmonto que usted desea retirar no puede ser retirado"+"\n");
            }
    }

            System.out.println("El sldo final es de"+oAccount.getSaldoinicial());
            System.out.println("Desea continuar con otra transaccion S/N"+"\n");
            continuar=teclado.nextLine().charAt(0);
            if((continuar=='S')||(continuar=='s')){
                validar=true;
            }
        if ((continuar=='N')||(continuar=='N')){
            validar=true;
        }
    }
}
