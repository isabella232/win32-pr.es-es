---
description: Es posible que la aplicación tenga que solicitar al usuario la información de nombre de usuario y contraseña para evitar almacenar una contraseña de administrador o comprobar que el token contiene los privilegios adecuados.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Solicitar credenciales al usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adb315837d86a9f1dda4075b8d89db33f0dd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668234"
---
# <a name="asking-the-user-for-credentials"></a><span data-ttu-id="74bda-103">Solicitar credenciales al usuario</span><span class="sxs-lookup"><span data-stu-id="74bda-103">Asking the User for Credentials</span></span>

<span data-ttu-id="74bda-104">Es posible que la aplicación tenga que solicitar al usuario la información de nombre de usuario y contraseña para evitar almacenar una contraseña de administrador o comprobar que el token contiene los privilegios adecuados.</span><span class="sxs-lookup"><span data-stu-id="74bda-104">Your application may need to prompt the user for user name and password information to avoid storing an administrator password or to verify that the token holds the appropriate privileges.</span></span>

<span data-ttu-id="74bda-105">Sin embargo, simplemente solicitar credenciales puede entrenar a los usuarios para que proporcionen a los cuadros de diálogo aleatorios no identificados que aparecen en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="74bda-105">However, simply prompting for credentials may train users to supply those to any random, unidentified dialog box that appears on the screen.</span></span> <span data-ttu-id="74bda-106">Se recomienda el procedimiento siguiente para reducir el efecto de entrenamiento.</span><span class="sxs-lookup"><span data-stu-id="74bda-106">The following procedure is recommended to reduce that training effect.</span></span>

<span data-ttu-id="74bda-107">**Para adquirir correctamente las credenciales de usuario**</span><span class="sxs-lookup"><span data-stu-id="74bda-107">**To properly acquire user credentials**</span></span>

1.  <span data-ttu-id="74bda-108">Informe al usuario mediante un mensaje que forma claramente parte de la aplicación, que verá un cuadro de diálogo que solicita su nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="74bda-108">Inform the user, by using a message that is clearly part of your application, that they will see a dialog box that requests their user name and password.</span></span> <span data-ttu-id="74bda-109">También puede usar la estructura [**CREDUI \_ info**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) en la llamada a [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para transmitir datos de identificación o un mensaje.</span><span class="sxs-lookup"><span data-stu-id="74bda-109">You can also use the [**CREDUI\_INFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) structure on the call to [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to convey identifying data or a message.</span></span>
2.  <span data-ttu-id="74bda-110">Llame a [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="74bda-110">Call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span></span> <span data-ttu-id="74bda-111">Tenga en cuenta que el número máximo de caracteres especificado para la información de nombre de usuario y contraseña incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="74bda-111">Note that the maximum number of characters specified for user name and password information includes the terminating null character.</span></span>
3.  <span data-ttu-id="74bda-112">Llame a [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) y [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) para comprobar que obtuvo las credenciales adecuadas.</span><span class="sxs-lookup"><span data-stu-id="74bda-112">Call [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) and [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) to verify that you obtained appropriate credentials.</span></span>

<span data-ttu-id="74bda-113">En el ejemplo siguiente se muestra cómo llamar a [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para pedir al usuario un nombre de usuario y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="74bda-113">The following example shows how to call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to ask the user for a user name and password.</span></span> <span data-ttu-id="74bda-114">Comienza rellenando una estructura de \_ información CREDUI con información sobre las solicitudes que se deben usar.</span><span class="sxs-lookup"><span data-stu-id="74bda-114">It begins by filling in a CREDUI\_INFO structure with information about what prompts to use.</span></span> <span data-ttu-id="74bda-115">A continuación, el código rellena dos búferes con ceros.</span><span class="sxs-lookup"><span data-stu-id="74bda-115">Next, the code fills two buffers with zeros.</span></span> <span data-ttu-id="74bda-116">Esto se hace para asegurarse de que no se pase información a la función que pueda revelar un nombre de usuario o contraseña antiguos al usuario.</span><span class="sxs-lookup"><span data-stu-id="74bda-116">This is done to ensure that no information gets passed to the function that might reveal an old user name or password to the user.</span></span> <span data-ttu-id="74bda-117">La llamada a **CredUIPromptForCredentials** muestra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="74bda-117">The call to **CredUIPromptForCredentials** brings up the dialog box.</span></span> <span data-ttu-id="74bda-118">Por motivos de seguridad, en este ejemplo se usa la \_ marca CREDUI Flags \_ \_ no \_ Persist para evitar que el sistema operativo almacene la contraseña, ya que podría exponerse.</span><span class="sxs-lookup"><span data-stu-id="74bda-118">For security reasons, this example uses the CREDUI\_FLAGS\_DO\_NOT\_PERSIST flag to prevent the operating system from storing the password because it might then be exposed.</span></span> <span data-ttu-id="74bda-119">Si no hay ningún error, **CredUIPromptForCredentials** rellena las variables pszName empiezan y pszPwd y devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="74bda-119">If there are no errors, **CredUIPromptForCredentials** fills in the pszName and pszPwd variables and returns zero.</span></span> <span data-ttu-id="74bda-120">Cuando la aplicación ha terminado de usar las credenciales, debe colocar ceros en los búferes para evitar que la información se revele accidentalmente.</span><span class="sxs-lookup"><span data-stu-id="74bda-120">When the application has finished using the credentials, it should put zeros in the buffers to prevent the information from being accidentally revealed.</span></span>


```C++
CREDUI_INFO cui;
TCHAR pszName[CREDUI_MAX_USERNAME_LENGTH+1];
TCHAR pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1];
BOOL fSave;
DWORD dwErr;
 
cui.cbSize = sizeof(CREDUI_INFO);
cui.hwndParent = NULL;
//  Ensure that MessageText and CaptionText identify what credentials
//  to use and which application requires them.
cui.pszMessageText = TEXT("Enter administrator account information");
cui.pszCaptionText = TEXT("CredUITest");
cui.hbmBanner = NULL;
fSave = FALSE;
SecureZeroMemory(pszName, sizeof(pszName));
SecureZeroMemory(pszPwd, sizeof(pszPwd));
dwErr = CredUIPromptForCredentials( 
    &cui,                         // CREDUI_INFO structure
    TEXT("TheServer"),            // Target for credentials
                                  //   (usually a server)
    NULL,                         // Reserved
    0,                            // Reason
    pszName,                      // User name
    CREDUI_MAX_USERNAME_LENGTH+1, // Max number of char for user name
    pszPwd,                       // Password
    CREDUI_MAX_PASSWORD_LENGTH+1, // Max number of char for password
    &fSave,                       // State of save check box
    CREDUI_FLAGS_GENERIC_CREDENTIALS |  // flags
    CREDUI_FLAGS_ALWAYS_SHOW_UI |
    CREDUI_FLAGS_DO_NOT_PERSIST);  

if(!dwErr)
{
    //  Put code that uses the credentials here.
 
    //  When you have finished using the credentials,
    //  erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
}
```



## <a name="related-topics"></a><span data-ttu-id="74bda-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74bda-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74bda-122">**CredUICmdLinePromptForCredentials**</span><span class="sxs-lookup"><span data-stu-id="74bda-122">**CredUICmdLinePromptForCredentials**</span></span>](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[<span data-ttu-id="74bda-123">**CREDUI \_ UINFO**</span><span class="sxs-lookup"><span data-stu-id="74bda-123">**CREDUI\_UINFO**</span></span>](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
