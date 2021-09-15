---
title: Método IConfigAsfWriter ConfigureFilterUsingProfileGuid
description: El método ConfigureFilterUsingProfileGuid configura el filtro para escribir un archivo ASF basado en el perfil predefinido especificado. (En desuso).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Método ConfigureFilterUsingProfileGuid windows Media Format
- Método ConfigureFilterUsingProfileGuid windows Media Format , interfaz IConfigAsfWriter
- IConfigAsfWriter interface windows Media Format , ConfigureFilterUsingProfileGuid method
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466492"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>IConfigAsfWriter::ConfigureFilterUsingProfileGuid (método)

El **método ConfigureFilterUsingProfileGuid** configura el filtro para escribir un archivo ASF basado en el perfil predefinido especificado. (En desuso).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*guidProfile* \[ En\]
</dt> <dd>

**GUID** que identifica un perfil tal como se define en el archivo de encabezado wmsysprf.h del SDK Windows media format.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT.**



| Código devuelto                                                                                         | Descripción                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | El método se ha llevado a cabo de forma correcta.<br/>        |
| <dl> <dt>**E \_ FAIL**</dt> </dl>              | El perfil no es válido.<br/>    |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ INCORRECTO**</dt> </dl> | El gráfico de filtro se detiene.<br/> |



 

## <a name="remarks"></a>Observaciones

A partir de Windows SDK de la serie Media Format 9, no se han definido nuevos perfiles del sistema. Con este método solo se pueden usar GUID de perfil de sistema de la versión 8 (o anterior).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConfigAsfWriter (Interfaz)**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

