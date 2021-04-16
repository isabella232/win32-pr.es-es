---
title: Creación de una nueva cuenta de equipo
description: En el siguiente ejemplo de código se muestra cómo crear una nueva cuenta de equipo mediante la función NetUserAdd.
ms.assetid: 1e180b8e-b948-4836-b789-cb9dff0829e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd02a9d2053310c50e40957e6afee6e3a4a5ab1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676398"
---
# <a name="creating-a-new-computer-account"></a>Creación de una nueva cuenta de equipo

En el siguiente ejemplo de código se muestra cómo crear una nueva cuenta de equipo mediante la función [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) .

A continuación se incluyen consideraciones para la administración de cuentas de equipo:

-   El nombre de la cuenta de equipo debe ser todo en mayúsculas para mantener la coherencia con las utilidades de administración de cuentas.
-   Un nombre de cuenta de equipo siempre tiene un signo de dólar ($) final. Cualquier función usada para administrar cuentas de equipo debe generar el nombre del equipo de modo que el último carácter del nombre de la cuenta de equipo sea un signo de dólar ($). En el caso de la confianza entre dominios, el nombre de cuenta es nombreDeDominioQueConfía $.
-   La longitud máxima del nombre del equipo es la longitud máxima de \_ NombreDeEquipo \_ (15). Esta longitud no incluye el signo de dólar ($) final.
-   La contraseña de una cuenta de equipo nueva debe ser la representación en minúsculas del nombre de la cuenta de equipo, sin el signo de dólar ($) final. Para la confianza entre dominios, la contraseña puede ser un valor arbitrario que coincida con el valor especificado en el lado de confianza de la relación.
-   La longitud máxima de la contraseña es LM20 \_ PWLEN (14). La contraseña debe truncarse a esta longitud si el nombre de la cuenta de equipo supera esta longitud.
-   La contraseña proporcionada en la hora de creación de la cuenta de equipo solo es válida hasta que se active la cuenta de equipo en el dominio. Durante la activación de la relación de confianza se establece una nueva contraseña.


```C++
#include <windows.h>
#include <lm.h>
#pragma comment(lib, "netapi32.lib")

BOOL AddMachineAccount(
    LPWSTR wTargetComputer,
    LPWSTR MachineAccount,
    DWORD AccountType
    )
{
    LPWSTR wAccount;
    LPWSTR wPassword;
    USER_INFO_1 ui;
    DWORD cbAccount;
    DWORD cbLength;
    DWORD dwError;

    //
    // Ensure a valid computer account type was passed.
    //
    if (AccountType != UF_WORKSTATION_TRUST_ACCOUNT &&
        AccountType != UF_SERVER_TRUST_ACCOUNT &&
        AccountType != UF_INTERDOMAIN_TRUST_ACCOUNT
        ) 
    {
        SetLastError(ERROR_INVALID_PARAMETER);
        return FALSE;
    }

    //
    // Obtain number of chars in computer account name.
    //
    cbLength = cbAccount = lstrlenW(MachineAccount);

    //
    // Ensure computer name doesn't exceed maximum length.
    //
    if(cbLength > MAX_COMPUTERNAME_LENGTH) {
        SetLastError(ERROR_INVALID_ACCOUNT_NAME);
        return FALSE;
    }

    //
    // Allocate storage to contain Unicode representation of
    // computer account name + trailing $ + NULL.
    //
    wAccount=(LPWSTR)HeapAlloc(GetProcessHeap(), 0,
        (cbAccount + 1 + 1) * sizeof(WCHAR)  // Account + '$' + NULL
        );

    if(wAccount == NULL) return FALSE;

    //
    // Password is the computer account name converted to lowercase;
    //  you will convert the passed MachineAccount in place.
    //
    wPassword = MachineAccount;

    //
    // Copy MachineAccount to the wAccount buffer allocated while
    //  converting computer account name to uppercase.
    //  Convert password (in place) to lowercase.
    //
    while(cbAccount--) {
        wAccount[cbAccount] = towupper( MachineAccount[cbAccount] );
        wPassword[cbAccount] = towlower( wPassword[cbAccount] );
    }

    //
    // Computer account names have a trailing Unicode '$'.
    //
    wAccount[cbLength] = L'$';
    wAccount[cbLength + 1] = L'\0'; // terminate the string

    //
    // If the password is greater than the max allowed, truncate.
    //
    if(cbLength > LM20_PWLEN) wPassword[LM20_PWLEN] = L'\0';

    //
    // Initialize the USER_INFO_1 structure.
    //
    ZeroMemory(&ui, sizeof(ui));

    ui.usri1_name = wAccount;
    ui.usri1_password = wPassword;

    ui.usri1_flags = AccountType | UF_SCRIPT;
    ui.usri1_priv = USER_PRIV_USER;

    dwError=NetUserAdd(
                wTargetComputer,    // target computer name
                1,                  // info level
                (LPBYTE) &ui,       // buffer
                NULL
                );

    //
    // Free allocated memory.
    //
    if(wAccount) HeapFree(GetProcessHeap(), 0, wAccount);

    //
    // Indicate whether the function was successful.
    //
    if(dwError == NO_ERROR)
        return TRUE;
    else {
        SetLastError(dwError);
        return FALSE;
    }
}
```



El usuario que llama a las funciones de administración de cuentas debe tener privilegios de administrador en el equipo de destino. En el caso de las cuentas de equipo existentes, el creador de la cuenta puede administrarla, independientemente de la pertenencia administrativa. Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).

El SeMachineAccountPrivilege se puede conceder en el equipo de destino para proporcionar a los usuarios especificados la capacidad de crear cuentas de equipo. Esto proporciona a los usuarios que no son administradores la capacidad de crear cuentas de equipo. El autor de la llamada debe habilitar este privilegio antes de agregar la cuenta de equipo. Para obtener más información sobre los privilegios de cuenta, vea [privilegios](/windows/desktop/SecAuthZ/privileges) y [constantes de autorización](/windows/desktop/SecAuthZ/authorization-constants).

 

 