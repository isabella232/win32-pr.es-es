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
# <a name="creating-a-new-computer-account"></a><span data-ttu-id="27eb6-103">Creación de una nueva cuenta de equipo</span><span class="sxs-lookup"><span data-stu-id="27eb6-103">Creating a New Computer Account</span></span>

<span data-ttu-id="27eb6-104">En el siguiente ejemplo de código se muestra cómo crear una nueva cuenta de equipo mediante la función [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) .</span><span class="sxs-lookup"><span data-stu-id="27eb6-104">The following code sample demonstrates how to create a new computer account using the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) function.</span></span>

<span data-ttu-id="27eb6-105">A continuación se incluyen consideraciones para la administración de cuentas de equipo:</span><span class="sxs-lookup"><span data-stu-id="27eb6-105">The following are considerations for managing computer accounts:</span></span>

-   <span data-ttu-id="27eb6-106">El nombre de la cuenta de equipo debe ser todo en mayúsculas para mantener la coherencia con las utilidades de administración de cuentas.</span><span class="sxs-lookup"><span data-stu-id="27eb6-106">The computer account name should be all uppercase for consistency with account management utilities.</span></span>
-   <span data-ttu-id="27eb6-107">Un nombre de cuenta de equipo siempre tiene un signo de dólar ($) final.</span><span class="sxs-lookup"><span data-stu-id="27eb6-107">A computer account name always has a trailing dollar sign ($).</span></span> <span data-ttu-id="27eb6-108">Cualquier función usada para administrar cuentas de equipo debe generar el nombre del equipo de modo que el último carácter del nombre de la cuenta de equipo sea un signo de dólar ($).</span><span class="sxs-lookup"><span data-stu-id="27eb6-108">Any functions used to manage computer accounts must build the computer name such that the last character of the computer account name is a dollar sign ($).</span></span> <span data-ttu-id="27eb6-109">En el caso de la confianza entre dominios, el nombre de cuenta es nombreDeDominioQueConfía $.</span><span class="sxs-lookup"><span data-stu-id="27eb6-109">For interdomain trust, the account name is TrustingDomainName$.</span></span>
-   <span data-ttu-id="27eb6-110">La longitud máxima del nombre del equipo es la longitud máxima de \_ NombreDeEquipo \_ (15).</span><span class="sxs-lookup"><span data-stu-id="27eb6-110">The maximum computer name length is MAX\_COMPUTERNAME\_LENGTH (15).</span></span> <span data-ttu-id="27eb6-111">Esta longitud no incluye el signo de dólar ($) final.</span><span class="sxs-lookup"><span data-stu-id="27eb6-111">This length does not include the trailing dollar sign ($).</span></span>
-   <span data-ttu-id="27eb6-112">La contraseña de una cuenta de equipo nueva debe ser la representación en minúsculas del nombre de la cuenta de equipo, sin el signo de dólar ($) final.</span><span class="sxs-lookup"><span data-stu-id="27eb6-112">The password for a new computer account should be the lowercase representation of the computer account name, without the trailing dollar sign ($).</span></span> <span data-ttu-id="27eb6-113">Para la confianza entre dominios, la contraseña puede ser un valor arbitrario que coincida con el valor especificado en el lado de confianza de la relación.</span><span class="sxs-lookup"><span data-stu-id="27eb6-113">For interdomain trust, the password can be an arbitrary value that matches the value specified on the trust side of the relationship.</span></span>
-   <span data-ttu-id="27eb6-114">La longitud máxima de la contraseña es LM20 \_ PWLEN (14).</span><span class="sxs-lookup"><span data-stu-id="27eb6-114">The maximum password length is LM20\_PWLEN (14).</span></span> <span data-ttu-id="27eb6-115">La contraseña debe truncarse a esta longitud si el nombre de la cuenta de equipo supera esta longitud.</span><span class="sxs-lookup"><span data-stu-id="27eb6-115">The password should be truncated to this length if the computer account name exceeds this length.</span></span>
-   <span data-ttu-id="27eb6-116">La contraseña proporcionada en la hora de creación de la cuenta de equipo solo es válida hasta que se active la cuenta de equipo en el dominio.</span><span class="sxs-lookup"><span data-stu-id="27eb6-116">The password provided at computer-account-creation time is valid only until the computer account becomes active on the domain.</span></span> <span data-ttu-id="27eb6-117">Durante la activación de la relación de confianza se establece una nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="27eb6-117">A new password is established during trust relationship activation.</span></span>


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



<span data-ttu-id="27eb6-118">El usuario que llama a las funciones de administración de cuentas debe tener privilegios de administrador en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="27eb6-118">The user that calls the account management functions must have Administrator privilege on the target computer.</span></span> <span data-ttu-id="27eb6-119">En el caso de las cuentas de equipo existentes, el creador de la cuenta puede administrarla, independientemente de la pertenencia administrativa.</span><span class="sxs-lookup"><span data-stu-id="27eb6-119">In the case of existing computer accounts, the creator of the account can manage the account, regardless of administrative membership.</span></span> <span data-ttu-id="27eb6-120">Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="27eb6-120">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="27eb6-121">El SeMachineAccountPrivilege se puede conceder en el equipo de destino para proporcionar a los usuarios especificados la capacidad de crear cuentas de equipo.</span><span class="sxs-lookup"><span data-stu-id="27eb6-121">The SeMachineAccountPrivilege can be granted on the target computer to give specified users the ability to create computer accounts.</span></span> <span data-ttu-id="27eb6-122">Esto proporciona a los usuarios que no son administradores la capacidad de crear cuentas de equipo.</span><span class="sxs-lookup"><span data-stu-id="27eb6-122">This gives non-administrators the ability to create computer accounts.</span></span> <span data-ttu-id="27eb6-123">El autor de la llamada debe habilitar este privilegio antes de agregar la cuenta de equipo.</span><span class="sxs-lookup"><span data-stu-id="27eb6-123">The caller needs to enable this privilege prior to adding the computer account.</span></span> <span data-ttu-id="27eb6-124">Para obtener más información sobre los privilegios de cuenta, vea [privilegios](/windows/desktop/SecAuthZ/privileges) y [constantes de autorización](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="27eb6-124">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

 

 