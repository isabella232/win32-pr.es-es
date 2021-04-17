---
description: Personalizar el comportamiento de Winlogon implementando un proveedor de credenciales.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personalización de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648223"
---
# <a name="customizing-winlogon"></a>Personalización de Winlogon

Personalizar el comportamiento de [*Winlogon*](/windows/desktop/SecGloss/w-gly) implementando un proveedor de credenciales. Para obtener información sobre los proveedores de credenciales, consulte [**ICredentialProvider (interfaz**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider)).

**Windows Server 2003 y Windows XP:** No se admiten proveedores de credenciales.

En las secciones siguientes se describen las distintas formas de personalizar Winlogon en versiones de Windows anteriores a Windows Vista.

> [!Note]  
> Los paquetes dll de GINA y de notificación de Winlogon se omiten en Windows Vista.

 

-   [Paquetes de notificación de Winlogon](#winlogon-notification-packages)
-   [Código auxiliar de GINA](#gina-stubs)
-   [Enlaces de GINA](#gina-hooks)

## <a name="winlogon-notification-packages"></a>Paquetes de notificación de Winlogon

Un paquete de notificación de Winlogon es un archivo DLL que exporta funciones que controlan eventos de Winlogon. Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a cada paquete de notificación para proporcionar información sobre el evento. Para obtener más información, consulte [paquetes de notificación de Winlogon](winlogon-notification-packages.md).

## <a name="gina-stubs"></a>Código auxiliar de GINA

Un código auxiliar de [*Gina*](/windows/desktop/SecGloss/g-gly) es un archivo dll de Gina personalizado que usa las implementaciones de la función de exportación de un archivo dll de Gina instalado previamente (normalmente MsGina.dll). Un código auxiliar GINA obtiene punteros a cada una de las funciones exportadas por el archivo DLL de GINA instalado previamente. Cada función de código auxiliar de GINA usa el puntero de función adecuado para llamar a la función correspondiente en el archivo DLL de GINA instalado previamente.

> [!IMPORTANT]
> Cada función de código auxiliar de GINA debe llamar a la función correspondiente en el GINA instalado previamente.

 

Una función de código auxiliar GINA puede implementar funcionalidad adicional en una o varias de sus funciones de exportación. Por ejemplo, la función [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) de un código auxiliar de Gina podría comprobar la hora actual antes de llamar a la función **WlxLoggedOutSAS** del MsGina.dll. Si la hora actual estaba dentro de un intervalo específico, la función de código auxiliar podría mostrar un mensaje que indica que no se permite el inicio de sesión durante ese período de tiempo y devolver **WLX \_ SAS \_ Action \_ None** a Winlogon. A continuación, se llamará a la función **WlxLoggedOutSAS** del MsGina.dll solo durante el período de tiempo permitido.

La aplicación de código auxiliar de GINA obtiene una tabla de envío para que las funciones de Winlogon admitan las funciones mediante el parámetro *pWinlogonFunctions* de la función [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) . La aplicación de código auxiliar de GINA puede utilizar esta tabla de envío para llamar a las funciones de compatibilidad de Winlogon. Por ejemplo, una aplicación de código auxiliar de GINA puede llamar a la función [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) para que se produzca un evento de [*secuencia de atención segura*](/windows/desktop/SecGloss/s-gly) (SAS) cuando se inserta una [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly) en un [*lector*](/windows/desktop/SecGloss/r-gly).

Para obtener más información sobre cómo crear un código auxiliar de GINA, vea el ejemplo de código auxiliar de Gina en el \\ \\ \\ \\ directorio Gina GinaStub Security de la instalación del kit de desarrollo de software (SDK) de la plataforma.

> [!Note]  
> Todas las llamadas entre GINA y Winlogon deben estar dentro de un solo subproceso.

 

## <a name="gina-hooks"></a>Enlaces de GINA

Un enlace GINA es un código auxiliar de GINA que, en su implementación de la función [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) , reemplaza el puntero a la función [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support en la tabla Dispatch con un puntero a su propia implementación de la función **WlxDialogBoxParam** . Como resultado, cada vez que el GINA instalado previamente (normalmente MsGina.dll) llama a la función **WlxDialogBoxParam** , se llama a la función implementada por el enlace gina.

La función [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) que implementa el enlace Gina puede reemplazar el procedimiento de devolución de llamada [**función dialogproc**](/windows/win32/api/winuser/nc-winuser-dlgproc) que responde a un evento de cuadro de diálogo específico.

Esto proporciona al enlace de GINA control total sobre la apariencia y el comportamiento de todos los cuadros de diálogo que crea MsGina.dll.

Para obtener más información sobre cómo crear un enlace GINA, consulte el ejemplo de enlaces de Gina en el \\ \\ \\ \\ Directorio de ejemplos de GinaHook de seguridad de la instalación de un SDK de la plataforma.

> [!Note]  
> Todas las llamadas entre GINA y Winlogon deben estar dentro de un solo subproceso.

 

 

 
