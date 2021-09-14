---
title: Crear una nueva cuenta de equipo
description: En el ejemplo de código siguiente se muestra cómo crear una nueva cuenta de equipo mediante la función NetUserAdd.
ms.assetid: 1e180b8e-b948-4836-b789-cb9dff0829e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd02a9d2053310c50e40957e6afee6e3a4a5ab1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169358"
---
# <a name="creating-a-new-computer-account"></a>Crear una nueva cuenta de equipo

En el ejemplo de código siguiente se muestra cómo crear una nueva cuenta de equipo mediante la [**función NetUserAdd.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)

Las siguientes son consideraciones para administrar cuentas de equipo:

-   El nombre de la cuenta de equipo debe estar en mayúsculas para mantener la coherencia con las utilidades de administración de cuentas.
-   Un nombre de cuenta de equipo siempre tiene un signo de dólar final ($). Las funciones usadas para administrar cuentas de equipo deben crear el nombre del equipo de forma que el último carácter del nombre de la cuenta de equipo sea un signo de dólar ($). Para la confianza entre dominios, el nombre de la cuenta es TrustingDomainName$.
-   La longitud máxima del nombre de equipo es MAX \_ COMPUTERNAME \_ LENGTH (15). Esta longitud no incluye el signo de dólar final ($).
-   La contraseña de una nueva cuenta de equipo debe ser la representación en minúscula del nombre de la cuenta de equipo, sin el signo de dólar final ($). Para la confianza entre dominios, la contraseña puede ser un valor arbitrario que coincida con el valor especificado en el lado de confianza de la relación.
-   La longitud máxima de la contraseña es \_ LM20 PWLEN (14). La contraseña debe truncarse a esta longitud si el nombre de la cuenta de equipo supera esta longitud.
-   La contraseña proporcionada en el momento de la creación de la cuenta de equipo solo es válida hasta que la cuenta de equipo se activa en el dominio. Se establece una nueva contraseña durante la activación de la relación de confianza.


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



El usuario que llama a las funciones de administración de cuentas debe tener privilegios de administrador en el equipo de destino. En el caso de las cuentas de equipo existentes, el creador de la cuenta puede administrar la cuenta, independientemente de la pertenencia administrativa. Para obtener más información sobre cómo llamar a funciones que requieren privilegios de administrador, vea [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).

Se puede conceder SeMachineAccountPrivilege en el equipo de destino para proporcionar a los usuarios especificados la capacidad de crear cuentas de equipo. Esto ofrece a los usuarios que no son administradores la capacidad de crear cuentas de equipo. El autor de la llamada debe habilitar este privilegio antes de agregar la cuenta de equipo. Para obtener más información sobre los privilegios de cuenta, vea [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).

 

 