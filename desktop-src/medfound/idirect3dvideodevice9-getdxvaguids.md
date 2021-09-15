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
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572856"
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

En la entrada, especifica el número de elementos de la *matriz pGuids.* Si *pGuids* **es NULL,** el valor de `*pNumGuids` debe ser cero.

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
| Encabezado<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 
