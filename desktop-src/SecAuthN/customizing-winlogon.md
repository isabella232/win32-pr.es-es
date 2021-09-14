---
description: Personalice el comportamiento de Winlogon implementando un Proveedor de credenciales.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personalización de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244377"
---
# <a name="customizing-winlogon"></a>Personalización de Winlogon

Personalice [*el comportamiento de Winlogon*](/windows/desktop/SecGloss/w-gly) implementando un Proveedor de credenciales. Para obtener información sobre los proveedores de credenciales, vea [**ICredentialProvider (Interfaz).**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider)

**Windows Server 2003 y Windows XP:** No se admiten proveedores de credenciales.

En las secciones siguientes se describen maneras de personalizar Winlogon en Windows versiones anteriores a Windows Vista.

> [!Note]  
> Los archivos DLL de GINA y los paquetes de notificación de Winlogon se omiten en Windows Vista.

 

-   [Paquetes de notificación de Winlogon](#winlogon-notification-packages)
-   [Códigos auxiliares de GINA](#gina-stubs)
-   [Enlaces de GINA](#gina-hooks)

## <a name="winlogon-notification-packages"></a>Paquetes de notificación de Winlogon

Un paquete de notificación de Winlogon es un archivo DLL que exporta funciones que controlan eventos winlogon. Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a cada paquete de notificación para proporcionar información sobre el evento. Para más información, consulte [Paquetes de notificación de Winlogon.](winlogon-notification-packages.md)

## <a name="gina-stubs"></a>Códigos auxiliares de GINA

Un [*código auxiliar de GINA*](/windows/desktop/SecGloss/g-gly) es un archivo DLL de GINA personalizado que usa las implementaciones de función de exportación de un archivo DLL de GINA instalado previamente (normalmente MsGina.dll). Un código auxiliar de GINA obtiene punteros a cada función exportada por el archivo DLL de GINA instalado anteriormente. A continuación, cada función de código auxiliar de GINA usa el puntero de función adecuado para llamar a la función correspondiente en el archivo DLL de GINA instalado anteriormente.

> [!IMPORTANT]
> Cada función de código auxiliar de GINA debe llamar a la función correspondiente en la GINA instalada anteriormente.

 

Una función de código auxiliar de GINA puede implementar funcionalidades adicionales en una o varias de sus funciones de exportación. Por ejemplo, la función [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) de un código auxiliar de GINA podría comprobar la hora actual antes de llamar a la función **WlxLoggedOutSAS** del MsGina.dll. Si la hora actual estaba dentro de un intervalo específico, la función de código auxiliar podría mostrar un mensaje que indica que el inicio de sesión no está permitido durante ese período de tiempo y devolver **WLX \_ SAS ACTION \_ \_ NONE** a Winlogon. La **función WlxLoggedOutSAS** del MsGina.dll llamaría solo durante el período de tiempo permitido.

La aplicación de código auxiliar GINA obtiene una tabla de distribución para las funciones de compatibilidad de Winlogon a través del *parámetro pWinlogonFunctions* de la [**función WlxInitialize.**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) La aplicación de código auxiliar GINA puede usar esta tabla de distribución para llamar a las funciones de soporte técnico de Winlogon. Por ejemplo, una aplicación de código auxiliar GINA puede llamar [*a*](/windows/desktop/SecGloss/s-gly) la función [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) para provocar un evento de secuencia de atención segura (SAS) cuando se inserta una tarjeta inteligente en un [*lector.*](/windows/desktop/SecGloss/r-gly) [](/windows/desktop/SecGloss/s-gly)

Para obtener más información sobre cómo crear un código auxiliar de GINA, consulte el ejemplo Gina Stubs en el directorio \\ \\ \\ Gina GinaStub de seguridad de ejemplos de una instalación del Kit de desarrollo de \\ software (SDK) de plataforma.

> [!Note]  
> Todas las llamadas entre GINA y Winlogon deben estar dentro de un único subproceso.

 

## <a name="gina-hooks"></a>Enlaces de GINA

Un enlace de GINA es un código auxiliar de GINA que, en su implementación de la función [**WlxInitialize,**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) reemplaza el puntero a la función de compatibilidad [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) de la tabla de distribución por un puntero a su propia implementación de la función **WlxDialogBoxParam.** Como resultado, cada vez que la GINA instalada anteriormente (normalmente MsGina.dll) llama a la **función WlxDialogBoxParam,** se llama a la función implementada por el enlace de GINA.

La [**función WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) implementada por el enlace GINA puede reemplazar el procedimiento de devolución de llamada [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) que responde a un evento de cuadro de diálogo específico.

Esto proporciona al enlace de GINA control total sobre la apariencia y el comportamiento de todos los cuadros de diálogo que MsGina.dll crea.

Para obtener más información sobre cómo crear un enlace de GINA, vea el ejemplo Gina Hooks en el directorio \\ \\ \\ Gina GinaHook de seguridad de ejemplos de una instalación \\ del SDK de plataforma.

> [!Note]  
> Todas las llamadas entre GINA y Winlogon deben estar dentro de un único subproceso.

 

 

 
