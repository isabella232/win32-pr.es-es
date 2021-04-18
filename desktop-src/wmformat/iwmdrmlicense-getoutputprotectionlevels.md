---
title: IWMDRMLicense GetOutputProtectionLevels, método
description: El método GetOutputProtectionLevels recupera información sobre todos los niveles de protección de salida (OPLs) asignados a la licencia.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Método GetOutputProtectionLevels formato de Windows Media
- Método GetOutputProtectionLevels formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método GetOutputProtectionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704831"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a>IWMDRMLicense:: GetOutputProtectionLevels (método)

El método **GetOutputProtectionLevels** recupera información sobre todos los niveles de protección de salida (OPLs) asignados a la licencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOPLs* \[ enuncia\]
</dt> <dd>

Puntero a una estructura de [**\_ niveles de \_ protección \_ de salida WMDRM**](wmdrm-output-protection-levels.md) que recibe la información de OPL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





