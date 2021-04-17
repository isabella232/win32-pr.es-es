---
title: Método IWMDRMLicenseManagement CleanLicenseStore (wmdrmsdk. h)
description: El método CleanLicenseStore quita las licencias inutilizables del almacén de licencias temporal y desfragmenta el almacén de licencias local para mejorar el rendimiento.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Método CleanLicenseStore formato de Windows Media
- Método CleanLicenseStore formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método CleanLicenseStore
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718674"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a>IWMDRMLicenseManagement:: CleanLicenseStore (método)

El método **CleanLicenseStore** quita las licencias inutilizables del almacén de licencias temporal y desfragmenta el almacén de licencias local para mejorar el rendimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Marcas que especifican las opciones de limpieza del almacén de licencias que se van a utilizar. Establezca en una de las constantes de la tabla siguiente.



| Constante                            | Descripción                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_sincronización del \_ almacén de licencias limpio \_ de WMDRM \_  | La operación de limpieza se realizará sincrónicamente. Este método no devolverá ningún resultado hasta que se complete la operación.                                                              |
| \_ \_ \_ almacenamiento asincrónico de licencias de WMDRM Clean \_ | La operación de limpieza se realizará de forma asincrónica. Este método devolverá inmediatamente. Una vez completada la operación, se enviará el evento MELicenseStoreCleaned. |



 

</dd> <dt>

*ppunkCancelationCookie* \[ enuncia\]
</dt> <dd>

Puntero que recibe un puntero a la interfaz **IUnknown** de un objeto que identifica esta llamada asincrónica. Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                            | Descripción                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | El método se ha llevado a cabo de forma correcta.<br/>                                       |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | No hay ningún almacén de licencias temporal en el equipo cliente.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método se ejecuta de forma asincrónica. Vuelve inmediatamente después de llamarlo y, a continuación, genera un evento **MEWMDRMLicenseStoreCleaned** cuando se completa el procesamiento.

Para obtener más información sobre el uso de los métodos asincrónicos de las API extendidas del cliente DRM de Windows Media, vea [usar el modelo de eventos de Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





