---
description: 'En el ejemplo siguiente se usa el método de adquisición de imágenes de Windows (WIA) 1,0 IWiaDevMgr:: RegisterEventCallbackCLSID para registrarse para recibir notificaciones cuando cualquier dispositivo de adquisición de imágenes de Windows (WIA) esté conectado al sistema.'
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: Registro para eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40fe29be23bda4a3094ff8bcf90ae1ca677e858d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154387"
---
# <a name="registering-for-events"></a>Registro para eventos

En el ejemplo siguiente se usa el método de adquisición de imágenes de Windows (WIA) 1,0 [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) para registrarse para recibir notificaciones cuando cualquier dispositivo de adquisición de imágenes de Windows (WIA) esté conectado al sistema. Las aplicaciones también pueden usar WIA 1,0 [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) y WIA 1,0 [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) para registrar eventos. Con Windows Vista y versiones posteriores, puede usar los métodos de adquisición de imágenes de Windows (WIA) 2,0 [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)o [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) para registrar eventos.

Se supone que el ejemplo se toma de una aplicación registrada como objeto de servidor fuera de proceso del modelo de objetos componentes (COM).

La llamada a [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (o [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) es la siguiente:


```
    pWiaDevMgr->RegisterEventCallbackCLSID( WIA_REGISTER_EVENT_CALLBACK,
                                            NULL,
                                            WIA_EVENT_DEVICE_CONNECTED,
                                            pCLSID,
                                            bstrName,
                                            bstrDescription,
                                            bstrIcon
                                            );
```



En el código anterior, **pWiaDevMgr** es un puntero válido a la interfaz [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)), la \_ devolución de llamada de evento de registro de WIA \_ \_ es una constante que especifica que esta llamada es registrarse para el evento en lugar de anular el registro para el evento, el \_ dispositivo de eventos WIA \_ \_ conectado es una constante que especifica que la aplicación se registra para recibir una notificación cada vez que un dispositivo está conectado **pCLSID** es un puntero al CLSID registrado de la aplicación, **bstrName** es el nombre de la aplicación, **bstrDescription** es una descripción de texto de la aplicación y **bstrIcon** es el nombre de un archivo de imagen que se va a utilizar para el icono de la aplicación que se registra para el evento.

A continuación, la aplicación debe implementar el método [**IWiaEventCallback:: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) , al que se llama cada vez que se produce un evento para el que se registra la aplicación.

Una aplicación puede usar el método [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (o [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) para enumerar la información sobre los eventos para los que se ha registrado.

 

 



