---
title: Método IWMDRMLicense GetAnalogVideoRestrictionLevels (wmdrmsdk. h)
description: El método GetAnalogVideoRestrictionLevels recupera todas las restricciones de vídeo analógico establecidas en la licencia actual.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Método GetAnalogVideoRestrictionLevels formato de Windows Media
- Método GetAnalogVideoRestrictionLevels formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetAnalogVideoRestrictionLevels
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
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708894"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a>IWMDRMLicense:: GetAnalogVideoRestrictionLevels (método)

El método **GetAnalogVideoRestrictionLevels** recupera todas las restricciones de vídeo analógico establecidas en la licencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*\[ rgAnalogVideoRestrictions \]* \[fuera de\]
</dt> <dd>

Recibe una matriz de estructuras de [**\_ \_ \_ restricciones de vídeo analógico WMDRM**](wmdrm-analog-video-restrictions.md) . Establezca en **null** para obtener el número de elementos de la matriz en *pcResctrictions*.

</dd> <dt>

*pcRestrictions* \[ in, out\]
</dt> <dd>

Número de elementos de la matriz de restricciones. Si *rgAnalogVideoRestrictions* se establece en **null**, este valor se establece en el número de elementos necesarios en la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Debe asignar memoria para la matriz de restricciones. Para ello, llame primero al método con *rgAnalogVideoRestrictions* establecido en **null**, que establecerá el valor de *pcRestrictions* en el número de elementos necesarios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





