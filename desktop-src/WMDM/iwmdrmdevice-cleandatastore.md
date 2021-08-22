---
title: Método IWMDRMDevice CleanDataStore
description: El método CleanDataStore inicia el proceso de limpieza del almacén de datos DRM en el dispositivo.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Método CleanDataStore windows Media Administrador de dispositivos
- Método CleanDataStore windows Media Administrador de dispositivos interfaz , IWMDRMDevice
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
ms.openlocfilehash: 9decc999d1ecb6c97359d1c4c169b84e7f67da88f5fa25bfe2cb17b2c31f9fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766645"
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMDevice (interfaz)**](iwmdrmdevice.md)
</dt> </dl>

 

 





