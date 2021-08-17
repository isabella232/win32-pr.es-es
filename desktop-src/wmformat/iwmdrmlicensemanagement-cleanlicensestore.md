---
title: Método IWMDRMLicenseManagement CleanLicenseStore (Wmdrmsdk.h)
description: El método CleanLicenseStore quita las licencias inutilizables del almacén de licencias temporal y desfragmenta el almacén de licencias local para mejorar el rendimiento.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Formato multimedia de Windows del método CleanLicenseStore
- Método CleanLicenseStore windows Media Format , interfaz IWMDRMLicenseManagement
- IWMDRMLicenseManagement interfaz windows Media Format , cleanLicenseStore (método)
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
ms.openlocfilehash: 6010313efaca6855c403f9ee698284ff4aebb2e0ab8a5e08e5862a5890224a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846962"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a>IWMDRMLicenseManagement::CleanLicenseStore (Método)

El **método CleanLicenseStore** quita las licencias inutilizables del almacén de licencias temporal y desfragmenta el almacén de licencias local para mejorar el rendimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Marcas que especifican las opciones de limpieza del almacén de licencias que se usarán. Establezca en una de las constantes de la tabla siguiente.



| Constante                            | Descripción                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ CLEAN \_ LICENSE \_ STORE \_ SYNC  | La operación de limpieza se realizará sincrónicamente. Este método no se devolverá hasta que se complete la operación.                                                              |
| WMDRM \_ CLEAN \_ LICENSE \_ STORE \_ ASYNC | La operación de limpieza se realizará de forma asincrónica. Este método devolverá inmediatamente. Una vez completada la operación, se enviará el evento multimedia MELicenseStoreCleaned. |



 

</dd> <dt>

*piqueCancelationCookie* \[ out\]
</dt> <dd>

Puntero que recibe un puntero a la **interfaz IUnknown** de un objeto que identifica esta llamada asincrónica. Este puntero de interfaz se puede usar para cancelar la llamada asincrónica llamando al [**método IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                            | Descripción                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | El método se ha llevado a cabo de forma correcta.<br/>                                       |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | No hay ningún almacén de licencias temporal en el equipo cliente.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método se ejecuta de forma asincrónica. Devuelve inmediatamente después de llamar a y, a continuación, genera un evento **MEWMDRMLicenseStoreCleaned** cuando se completa el procesamiento.

Para obtener más información sobre el uso de los métodos asincrónicos de Windows MEDIA DRM Client Extended API, vea [Using the Media Foundation Event Model](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





