---
title: IConfigAsfWriter GetCurrentProfileGuid, método
description: El método GetCurrentProfileGuid recupera el GUID actual del perfil del sistema de Windows Media.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Método GetCurrentProfileGuid formato de Windows Media
- Método GetCurrentProfileGuid formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método GetCurrentProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359304"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a>IConfigAsfWriter:: GetCurrentProfileGuid (método)

El método **GetCurrentProfileGuid** recupera el GUID actual del perfil del sistema de Windows Media.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProfileGuid* \[ enuncia\]
</dt> <dd>

Puntero a una variable de tipo **GUID** que identifica el perfil de sistema actual que usa el filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método no se utiliza con perfiles personalizados (incluidos todos los perfiles que incluyen secuencias que usan los códecs de vídeo y Windows Media Audio) porque todos estos perfiles se crean mediante aplicaciones y no tienen ningún identificador GUID. Si no se carga ningún perfil del sistema, *pProfileGuid* se establecerá en **null**.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 