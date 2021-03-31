---
title: IConfigAsfWriter ConfigureFilterUsingProfileGuid, método
description: El método ConfigureFilterUsingProfileGuid configura el filtro para escribir un archivo ASF basado en el perfil predefinido especificado. (Desusado).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Método ConfigureFilterUsingProfileGuid formato de Windows Media
- Método ConfigureFilterUsingProfileGuid formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método ConfigureFilterUsingProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533411"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>IConfigAsfWriter:: ConfigureFilterUsingProfileGuid (método)

El método **ConfigureFilterUsingProfileGuid** configura el filtro para escribir un archivo ASF basado en el perfil predefinido especificado. (En desuso).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*guidProfile* \[ de\]
</dt> <dd>

**GUID** que identifica un perfil tal y como se define en el archivo de encabezado del SDK de Windows Media Format Wmsysprf. h.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** .



| Código devuelto                                                                                         | Descripción                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                | El método se ha llevado a cabo de forma correcta.<br/>        |
| <dl> <dt>**E \_ FAIL**</dt> </dl>              | El perfil no es válido.<br/>    |
| <dl> <dt>**Estado de VFW \_ E \_ incorrecto \_**</dt> </dl> | El gráfico de filtro está detenido.<br/> |



 

## <a name="remarks"></a>Observaciones

A partir del SDK de Windows Media Format 9 series, no se ha definido ningún perfil del sistema nuevo. Con este método solo se pueden usar GUID de Perfil de sistema de la versión 8 (o anterior).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

