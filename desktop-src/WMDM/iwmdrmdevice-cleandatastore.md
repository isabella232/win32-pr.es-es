---
title: Método IWMDRMDevice CleanDataStore
description: El método CleanDataStore inicia el proceso de limpieza del almacén de datos DRM en el dispositivo.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Método CleanDataStore windows Media Administrador de dispositivos
- Método CleanDataStore de Windows Media Administrador de dispositivos , interfaz IWMDRMDevice
- Interfaz IWMDRMDevice windows Media Administrador de dispositivos , método CleanDataStore
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5aed9608a7428245edd84602ea5e7252861d938
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967844"
---
# <a name="iwmdrmdevicecleandatastore-method"></a>IWMDRMDevice::CleanDataStore (método)

El **método CleanDataStore** inicia el proceso de limpieza del almacén de datos DRM en el dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Marcas para los criterios de limpieza del almacén.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





