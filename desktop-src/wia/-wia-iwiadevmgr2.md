---
description: La interfaz IWiaDevMgr2 se usa para crear y administrar dispositivos de adquisición de imágenes y para registrarse para recibir eventos de dispositivo.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: Interfaz IWiaDevMgr2 (Wia.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262327"
---
# <a name="iwiadevmgr2-interface"></a>Interfaz IWiaDevMgr2

La **interfaz IWiaDevMgr2** se usa para crear y administrar dispositivos de adquisición de imágenes y para registrarse para recibir eventos de dispositivo.

## <a name="members"></a>Members

La **interfaz IWiaDevMgr2** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaDevMgr2 también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWiaDevMgr2 tiene** estos métodos.



| Método                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDevice**](-wia-iwiadevmgr2-createdevice.md)                                     | Crea un árbol jerárquico [**de objetos IWiaItem2**](-wia-iwiaitem2.md) para un dispositivo WIA 2.0. <br/>                                                                                                                                                                                                                                                                                                 |
| [**EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | Crea un enumerador de información de propiedades para cada dispositivo WIA 2.0 disponible. <br/>                                                                                                                                                                                                                                                                                                                 |
| [**GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md)                                       | El [**método IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) muestra uno o varios cuadros de diálogo que permiten a un usuario adquirir una imagen de un dispositivo WIA 2.0 y escribir la imagen en un archivo especificado. Este método amplía la funcionalidad de [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular la adquisición de imágenes en una sola llamada API. <br/> |
| [**RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | El [**método IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) registra una aplicación para recibir eventos incluso si la aplicación no se está ejecutando.<br/>                                                                                                                                                                                                      |
| [**RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) | Registra una aplicación en ejecución para la notificación de eventos de WIA 2.0. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | El [**método IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) registra una aplicación para recibir eventos de dispositivo. Se proporciona principalmente por compatibilidad con versiones anteriores con aplicaciones que no se escribieron para WIA 2.0.<br/>                                                                                                                         |
| [**SeleccioneDeviceDlg.**](-wia-iwiadevmgr2-selectdevicedlg.md)                               | Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes. <br/>                                                                                                                                                                                                                                                                                                   |
| [**SeleccioneDeviceDlgID.**](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes. <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

La **interfaz IWiaDevMgr2,** al igual que todas las interfaces del modelo de objetos componentes (COM), hereda los métodos de [interfaz IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Métodos IUnknown                                        | Descripción                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Devuelve punteros a las interfaces compatibles. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa el recuento de referencias.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Reduce el recuento de referencias.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
