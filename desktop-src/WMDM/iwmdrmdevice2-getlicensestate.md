---
title: Método IWMDRMDevice2 GetLicenseState
description: El método GetLicenseState obtiene el estado de la licencia.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Método GetLicenseState windows Media Administrador de dispositivos
- Método GetLicenseState windows Media Administrador de dispositivos interfaz , IWMDRMDevice2
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
ms.openlocfilehash: e068d537f460053800b0d52d667ba39b0577d717b08f83794a73b2bf8c854aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055703"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>IWMDRMDevice2::GetLicenseState (método)

El **método GetLicenseState** obtiene el estado de la licencia.

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

Puntero a los datos consultados del estado de la licencia.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMDevice2 (interfaz)**](iwmdrmdevice2.md)
</dt> </dl>

 

 





