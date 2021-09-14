---
title: Método IWMDRMDevice2 GetLicenseState
description: El método GetLicenseState obtiene el estado de licencia.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Método GetLicenseState de Windows Media Administrador de dispositivos
- Método GetLicenseState de Windows Media Administrador de dispositivos , interfaz IWMDRMDevice2
- Interfaz IWMDRMDevice2 windows Media Administrador de dispositivos , método GetLicenseState
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068502"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>IWMDRMDevice2::GetLicenseState (método)

El **método GetLicenseState** obtiene el estado de licencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbStateQueryData* \[ En\]
</dt> <dd>

Puntero a los datos consultados del estado de licencia.

</dd> <dt>

*cbStateQueryData* \[ En\]
</dt> <dd>

Recuento de los datos consultados.

</dd> <dt>

*pdwCategory* \[ out\]
</dt> <dd>

Puntero a la categoría.

</dd> <dt>

*pcRemainingCounts* \[ out\]
</dt> <dd>

Puntero a los recuentos restantes.

</dd> <dt>

*pcRemainingHours* \[ out\]
</dt> <dd>

Puntero a las horas restantes.

</dd> <dt>

*pdwReserved* \[ out\]
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se realiza correctamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





