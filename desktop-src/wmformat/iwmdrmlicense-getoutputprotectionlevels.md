---
title: Método IWMDRMLicense GetOutputProtectionLevels
description: El método GetOutputProtectionLevels recupera información sobre todos los niveles de protección de salida (OPL) asignados a la licencia.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Método GetOutputProtectionLevels windows Media Format
- Método GetOutputProtectionLevels windows Media Format , interfaz IWMDRMLicense
- IWMDRMLicense interface windows Media Format , GetOutputProtectionLevels method
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8d70aaae5e96b8328c091e49836ae743c0fd5ef9d5036fd5aca067f9305d7fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771325"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a>IWMDRMLicense::GetOutputProtectionLevels (método)

El **método GetOutputProtectionLevels** recupera información sobre todos los niveles de protección de salida (OPL) asignados a la licencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOPLs* \[ out\]
</dt> <dd>

Puntero a una [**estructura WMDRM \_ OUTPUT PROTECTION \_ \_ LEVELS**](wmdrm-output-protection-levels.md) que recibe la información de OPL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMLicense (Interfaz)**](iwmdrmlicense.md)
</dt> </dl>

 

 





