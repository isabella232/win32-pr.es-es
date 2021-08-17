---
description: Obtiene una lista de perfiles de aceleración de vídeo de DirectX (DXVA) compatibles con el controlador de pantalla.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: Método IDirect3DVideoDevice9::GetDXVAGuids (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 6a355c27177a546a2e91e769f72d9f4b9e216b005f711d42b5b7af39b4b78361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119269245"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a>IDirect3DVideoDevice9::GetDXVAGuids (método)

Obtiene una lista de perfiles de aceleración de vídeo de DirectX (DXVA) compatibles con el controlador de pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNumGuids* 
</dt> <dd>

En la entrada, especifica el número de elementos de la *matriz pGuids.* Si *pGuids* es **NULL,** el valor `*pNumGuids` de debe ser cero.

En la salida, *si pGuids* es **NULL,** *pNumGuids* recibe el número de perfiles DXVA en modo restringido. De lo *contrario, pNumGuids* recibe el número real de GUID que se copian en la *matriz pGuids.*

</dd> <dt>

*pGuids* 
</dt> <dd>

Dirección de una matriz de GUID o **NULL.** Si el valor no es **NULL,** la matriz recibe una lista de GUID que especifican perfiles DXVA en modo restringido. Estos GUID se definen en dxva.h y se documentan en la [especificación DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Llame a este método dos veces. En la primera llamada, establezca *pGuids* en **NULL.** El *parámetro pNumGuids* recibe el número de GUID de perfil dxva. Asigne una matriz de GUID con el tamaño necesario y vuelva a llamar al método. Esta vez, establezca *pGuids en* la dirección de la matriz. El método rellena la matriz con la lista de GUID de perfil dxva.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 
