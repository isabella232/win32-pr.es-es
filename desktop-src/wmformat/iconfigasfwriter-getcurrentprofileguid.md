---
title: IConfigAsfWriter GetCurrentProfileGuid (método)
description: El método GetCurrentProfileGuid recupera el GUID Windows perfil del sistema multimedia actual.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Método GetCurrentProfileGuid windows Media Format
- Método GetCurrentProfileGuid windows Media Format, interfaz IConfigAsfWriter
- IConfigAsfWriter interface windows Media Format , GetCurrentProfileGuid (método)
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae1c626658509d4260f814550c053de7389b0aed45c9c583e0e059e390a24f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433644"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>IConfigAsfWriter::GetCurrentProfileGuid (método)

El **método GetCurrentProfileGuid** recupera el GUID Windows perfil del sistema multimedia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProfileGuid* \[ out\]
</dt> <dd>

Puntero a una variable de tipo **GUID** que identifica el perfil del sistema actual utilizado por el filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método no se usa con perfiles personalizados (incluidos todos los perfiles que incluyen secuencias que usan los códecs de audio y vídeo multimedia de Windows) porque todos estos perfiles los crean las aplicaciones y no tienen ningún identificador GUID. Si no se carga ningún perfil del sistema, *pProfileGuid* se establecerá en **NULL.**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IConfigAsfWriter (Interfaz)**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 