---
title: IConfigAsfWriter GetCurrentProfile, método
description: El método GetCurrentProfile recupera el perfil definido por la aplicación.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Método GetCurrentProfile formato de Windows Media
- Método GetCurrentProfile formato de Windows Media, interfaz IConfigAsfWriter
- Interfaz IConfigAsfWriter formato de Windows Media, método GetCurrentProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714397"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>IConfigAsfWriter:: GetCurrentProfile (método)

El método **GetCurrentProfile** recupera el perfil definido por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppProfile* \[ enuncia\]
</dt> <dd>

Dirección de un puntero que recibe la interfaz [**IWMProfile**](iwmprofile.md) del perfil definido por la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Si el método se ejecuta correctamente, el puntero **IWMProfile** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 