---
title: IConfigAsfWriter GetCurrentProfileId, método
description: El método GetCurrentProfileId recupera el identificador de perfil actual. (Solo para perfiles de Windows Media Format 4,0).
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Método GetCurrentProfileId formato de Windows Media
- Método GetCurrentProfileId formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método GetCurrentProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695658"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a>IConfigAsfWriter:: GetCurrentProfileId (método)

El método **GetCurrentProfileId** recupera el identificador de perfil actual. (Solo para perfiles de Windows Media Format 4,0).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwProfileId* \[ enuncia\]
</dt> <dd>

Puntero a una variable de tipo **DWORD** que recibe el ID. de perfil actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método está ahora obsoleto porque supone la versión 4,0 perfiles de SDK de Windows Media Format. En su lugar, use [**IConfigAsfWriter:: GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) o [**IConfigAsfWriter:: GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) para identificar correctamente un perfil de la versión 7,0 y posteriores.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 