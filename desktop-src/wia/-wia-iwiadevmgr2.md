---
description: La interfaz IWiaDevMgr2 se usa para crear y administrar dispositivos de adquisición de imágenes y registrarse para recibir eventos de dispositivo.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: Interfaz IWiaDevMgr2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909865"
---
# <a name="iwiadevmgr2-interface"></a>Interfaz IWiaDevMgr2

La interfaz **IWiaDevMgr2** se usa para crear y administrar dispositivos de adquisición de imágenes y registrarse para recibir eventos de dispositivo.

## <a name="members"></a>Miembros

La interfaz **IWiaDevMgr2** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaDevMgr2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWiaDevMgr2** tiene estos métodos.



| Método                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDevice**](-wia-iwiadevmgr2-createdevice.md)                                     | Crea un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para un dispositivo WIA 2,0. <br/>                                                                                                                                                                                                                                                                                                 |
| [**EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | Crea un enumerador de información de propiedad para cada dispositivo WIA 2,0 disponible. <br/>                                                                                                                                                                                                                                                                                                                 |
| [**GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md)                                       | El método [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) muestra uno o varios cuadros de diálogo que permiten a un usuario adquirir una imagen de un dispositivo WIA 2,0 y escribir la imagen en un archivo especificado. Este método extiende la funcionalidad de [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular la adquisición de imágenes en una única llamada API. <br/> |
| [**RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | El método [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) registra una aplicación para recibir eventos incluso si la aplicación no se está ejecutando.<br/>                                                                                                                                                                                                      |
| [**RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) | Registra una aplicación en ejecución para la notificación de eventos de WIA 2,0. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | El método [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) registra una aplicación para recibir eventos de dispositivo. Se proporciona principalmente para la compatibilidad con versiones anteriores de aplicaciones que no se escribieron para WIA 2,0.<br/>                                                                                                                         |
| [**SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md)                               | Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes. <br/>                                                                                                                                                                                                                                                                                                   |
| [**SelectDeviceDlgID**](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes. <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

La interfaz **IWiaDevMgr2** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
