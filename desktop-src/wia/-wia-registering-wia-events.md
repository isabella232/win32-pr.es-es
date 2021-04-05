---
description: 'Las aplicaciones pueden registrarse para recibir notificaciones de eventos de dispositivo de hardware de adquisición de imágenes de Windows (WIA) mediante una llamada a uno de los siguientes métodos de interfaz IWiaDevMgr o IWiaDevMgr2: IWiaDevMgr:: RegisterEventCallbackCLSID o IWiaDevMgr2:: RegisterEventCallbackCLSIDIWiaDevMgr:: RegisterEventCallbackInterface o IWiaDevMgr2:: RegisterEventCallbackInterfaceIWiaDevMgr:: RegisterEventCallbackProgram o IWiaDevMgr2:: RegisterEventCallbackProgram'
ms.assetid: 0c142083-835f-4bbd-ab32-eb6130f99c59
title: Registrar eventos WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9fc36540a64211428579bc13b84902490ea103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001178"
---
# <a name="registering-wia-events"></a>Registrar eventos WIA

Las aplicaciones pueden registrarse para recibir notificaciones de eventos de dispositivo de hardware de adquisición de imágenes de Windows (WIA) mediante una llamada a uno de los siguientes métodos de interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) :

-   [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) o [ **IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)
-   [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) o [ **IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)
-   [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) o [ **IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)

Todos estos métodos toman parámetros que especifican el evento y el dispositivo de hardware para el que se va a notificar a la aplicación. Las aplicaciones se registran para recibir un evento para todos los dispositivos WIA pasando un valor **null** para el parámetro que especifica el dispositivo de hardware.

El método **RegisterEventCallbackInterface** registra una aplicación para recibir un evento de dispositivo de hardware WIA si la aplicación se está ejecutando en el momento en que se produce el evento. Cuando se produce el evento para el que se registra la aplicación, WIA llama al método [**IWiaEventCallback:: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) del objeto proporcionado por la aplicación para transmitir la información de evento.

El método **RegisterEventCallbackCLSID** registra una aplicación que es un componente del modelo de objetos componentes (com) registrado para recibir un evento de dispositivo de hardware WIA, incluso si la aplicación no se está ejecutando. Además de los parámetros mencionados anteriormente, este método toma un parámetro, *pClsID*, que especifica el identificador de clase de la aplicación. Cuando se produce el evento especificado, el sistema WIA usa la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y el identificador de clase especificado por *pClsID* para crear una nueva instancia de la aplicación y llama al método [**IWiaEventCallback:: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) de esa aplicación para transmitir la información de evento.

El método **RegisterEventCallbackProgram** registra una aplicación para recibir un evento de dispositivo de hardware WIA incluso si la aplicación no se está ejecutando cuando se produce el evento. No es necesario que la aplicación sea un componente COM registrado. WIA inicia la aplicación con una instrucción de línea de comandos. **RegisterEventCallbackProgram** toma un parámetro, *bstrCommandline*, que especifica la ruta de acceso completa y el nombre de archivo de la aplicación ejecutable. **RegisterEventCallbackProgram** existe por compatibilidad con versiones anteriores de aplicaciones que no se ESCRIBIERON para WIA y debe evitarse. Use **RegisterEventCallbackInterface** o **RegisterEventCallbackCLSID** en su lugar.

Para determinar qué controladores se registran para los eventos en un dispositivo WIA específico, una aplicación llama a un método [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) o [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) de un elemento raíz. Este método crea un objeto de enumeración para la información de registro. A continuación, la aplicación puede usar la interfaz [**IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) de ese objeto para enumerar información acerca de los controladores registrados para recibir eventos para ese dispositivo.

Si se produce un evento para el que se registra una aplicación en ejecución a través de **RegisterEventCallbackInterface** y de **RegisterEventCallbackCLSID** o **RegisterEventCallbackProgram**, WIA notifica a la aplicación en ejecución y no intenta iniciar una nueva instancia de la aplicación, ya que el registro de eventos a través de **RegisterEventCallbackInterface** tiene prioridad sobre **RegisterEventCallbackCLSID** y **RegisterEventCallbackProgram**.

> [!Note]  
> En una aplicación multiproceso, no hay ninguna garantía de que el subproceso devuelto por la devolución de llamada de notificación de eventos sea el mismo subproceso que registró la devolución de llamada.

 

 

 
