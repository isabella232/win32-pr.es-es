---
title: Método IConfigAsfWriter GetCurrentProfile
description: El método GetCurrentProfile recupera el perfil definido por la aplicación.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Formato multimedia de windows del método GetCurrentProfile
- Método GetCurrentProfile windows Media Format , interfaz IConfigAsfWriter
- IConfigAsfWriter interface windows Media Format , GetCurrentProfile (método)
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b7a07ed6ab5b94138c0c04d40782496535e0ae4a3eff0f443c89d7ccd0c4b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198386"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a>IConfigAsfWriter::GetCurrentProfile (método)

El **método GetCurrentProfile** recupera el perfil definido por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppProfile* \[ out\]
</dt> <dd>

Dirección de un puntero que recibe la [**interfaz IWMProfile**](iwmprofile.md) del perfil definido por la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Si el método se realiza correctamente, el **puntero IWMProfile** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IConfigAsfWriter (Interfaz)**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 