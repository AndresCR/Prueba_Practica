        boolean validar=true;
        int opcion;
        char continuar;
        double monto;

        Account oAccount=new Account();
        Scanner teclado=new Scanner(System.in);

        while(validar)
        {
            System.out.println("Digite 1 si quiere hacer un deposito y 2 si desea hacer un retiro");
            opcion=Integer.parseInt(teclado.nextLine());
            if(opcion==1){
                System.out.println("Digite el monto a depositar");
                monto=Double.parseDouble(teclado.nextLine());
                oAccount.Deposito(monto);
            }
            if(opcion==2){
                System.out.println("Digite el monto a retirar");
                monto=Double.parseDouble(teclado.nextLine());
                oAccount.Retiro(monto);
                if(oAccount.isHayError()){
                    System.out.println("Ese monto en superior a su saldo, debe retirar un monto inferior");
                }
            }
            System.out.println("El saldo final es:"+oAccount.getSaldoinicial());
            System.out.print("Desea continuar con otra transacción S/N"+"\n");
            continuar=teclado.nextLine().charAt(0);
            if((continuar=='s')||(continuar=='S')){
                validar=true;
            }
            if((continuar=='n')||(continuar=='N'))
                validar=false;
            }
                }
            }
