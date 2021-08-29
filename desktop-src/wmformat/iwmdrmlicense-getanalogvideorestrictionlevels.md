---
title: Método IWMDRMLicense GetAnalogVideoRestrictionLevels (Wmdrmsdk.h)
description: El método GetAnalogVideoRestrictionLevels recupera todas las restricciones de vídeo análogo establecidas en la licencia actual.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Método GetAnalogVideoRestrictionLevels windows Media Format
- Método GetAnalogVideoRestrictionLevels windows Media Format , interfaz IWMDRMLicense
- IWMDRMLicense interfaz windows Media Format , Método GetAnalogVideoRestrictionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1848165729b67a21ae65b506739ccf6d336f51afd51292bae7b66bcd067fdee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808675"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a>Método IWMDRMLicense::GetAnalogVideoRestrictionLevels

El **método GetAnalogVideoRestrictionLevels** recupera todas las restricciones de vídeo análogo establecidas en la licencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rgAnalogVideoRestrictions \[ \]* \[out\]
</dt> <dd>

Recibe una matriz de [**estructuras \_ DE WMDRM ANALOG VIDEO \_ \_ RESTRICTIONS.**](wmdrm-analog-video-restrictions.md) Establezca en **NULL** para obtener el número de elementos de la matriz en *pcResctrictions*.

</dd> <dt>

*pcRestrictions* \[ in, out\]
</dt> <dd>

Número de elementos de la matriz de restricciones. Si *rgAnalogVideoRestrictions* se establece en **NULL,** este valor se establece en el número de elementos necesarios en la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Debe asignar memoria para la matriz de restricciones. Para ello, primero llame al método con *rgAnalogVideoRestrictions* establecido en **NULL,** que establecerá el valor en *pcRestrictions* en el número de elementos necesarios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





