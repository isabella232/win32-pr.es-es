---
description: Es posible que la aplicación tenga que solicitar al usuario información de nombre de usuario y contraseña para evitar almacenar una contraseña de administrador o para comprobar que el token contiene los privilegios adecuados.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Pedir credenciales al usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adb315837d86a9f1dda4075b8d89db33f0dd22e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071195"
---
# <a name="asking-the-user-for-credentials"></a>Pedir credenciales al usuario

Es posible que la aplicación tenga que solicitar al usuario información de nombre de usuario y contraseña para evitar almacenar una contraseña de administrador o para comprobar que el token contiene los privilegios adecuados.

Sin embargo, simplemente solicitar credenciales puede entrenar a los usuarios para que los proporcionen a cualquier cuadro de diálogo aleatorio no identificado que aparezca en la pantalla. Se recomienda el procedimiento siguiente para reducir ese efecto de entrenamiento.

**Para adquirir correctamente las credenciales de usuario**

1.  Informe al usuario, mediante un mensaje que claramente forma parte de la aplicación, que verá un cuadro de diálogo que solicita su nombre de usuario y contraseña. También puede usar la estructura [**CREDUI \_ INFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) en la llamada a [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para transmitir datos de identificación o un mensaje.
2.  Llame [**a CredUIPromptForCredentials.**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) Tenga en cuenta que el número máximo de caracteres especificado para la información de nombre de usuario y contraseña incluye el carácter nulo de terminación.
3.  Llame [**a CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) y [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) para comprobar que ha obtenido las credenciales adecuadas.

En el ejemplo siguiente se muestra cómo llamar a [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) para pedir al usuario un nombre de usuario y una contraseña. Comienza rellenando una estructura DE INFORMACIÓN DE CREDUI \_ con información sobre las solicitudes que se deben usar. A continuación, el código rellena dos búferes con ceros. Esto se hace para asegurarse de que no se pasa información a la función que pueda revelar al usuario un nombre de usuario o una contraseña antiguos. La llamada a **CredUIPromptForCredentials** abre el cuadro de diálogo. Por motivos de seguridad, en este ejemplo se usa la marca CREDUI FLAGS DO NOT PERSIST para evitar que el sistema operativo almacene la contraseña porque podría \_ \_ \_ \_ exponerse. Si no hay errores, **CredUIPromptForCredentials** rellena las variables pszName y pszPwd y devuelve cero. Cuando la aplicación haya terminado de usar las credenciales, debe colocar ceros en los búferes para evitar que la información se revele accidentalmente.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[**CREDUI \_ UINFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
