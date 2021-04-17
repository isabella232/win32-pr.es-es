---
title: IWMDRMDevice2 GetLicenseState, método
description: El método GetLicenseState obtiene el estado de la licencia.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Método GetLicenseState de Windows Media Administrador de dispositivos
- Método GetLicenseState de Windows Media Administrador de dispositivos, interfaz IWMDRMDevice2
- Interfaz IWMDRMDevice2 de Windows Media Administrador de dispositivos, método GetLicenseState
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700416"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>IWMDRMDevice2:: GetLicenseState (método)

El método **GetLicenseState** obtiene el estado de la licencia.

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

*pbStateQueryData* \[ de\]
</dt> <dd>

Puntero a los datos consultados del estado de la licencia.

</dd> <dt>

*cbStateQueryData* \[ de\]
</dt> <dd>

Recuento de los datos consultados.

</dd> <dt>

*pdwCategory* \[ enuncia\]
</dt> <dd>

Puntero a la categoría.

</dd> <dt>

*pcRemainingCounts* \[ enuncia\]
</dt> <dd>

Puntero a los recuentos restantes.

</dd> <dt>

*pcRemainingHours* \[ enuncia\]
</dt> <dd>

Puntero al resto de horas.

</dd> <dt>

*pdwReserved* \[ enuncia\]
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ejecuta correctamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





