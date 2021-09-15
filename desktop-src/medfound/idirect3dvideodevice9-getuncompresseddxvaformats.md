---
description: Obtiene una lista de formatos de píxeles sin comprimir que se pueden representar mediante un perfil de aceleración de vídeo de DirectX (DXVA) especificado.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: Método IDirect3DVideoDevice9::GetUncompressedDXVAFormats (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579984"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a>IDirect3DVideoDevice9::GetUncompressedDXVAFormats (método)

Obtiene una lista de formatos de píxeles sin comprimir que se pueden representar mediante un perfil de aceleración de vídeo de DirectX (DXVA) especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGuid* 
</dt> <dd>

Puntero a un GUID que especifica el perfil dxva. Para obtener una lista de perfiles admitidos, llame a [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pNumFormats* 
</dt> <dd>

En la entrada, especifica el número de elementos de la matriz *pFormats.* Si *pFormats* es **NULL,** el valor de `*pNumFormats` debe ser cero.

En la salida, si *pFormats* es **NULL,** *pNumFormats* recibe el número de formatos de píxel admitidos. De lo contrario, *pNumFormats* recibe el número real de formatos de píxeles copiados en la *matriz pFormats.*

</dd> <dt>

*pFormats* 
</dt> <dd>

Dirección de una matriz de **valores D3DFORMAT** o **NULL.** Si el valor no es **NULL,** la matriz recibe una lista de formatos de píxel.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Llame a este método dos veces. En la primera llamada, establezca *pFormats* en **NULL.** El *parámetro pNumFormats* recibe el número de formatos. Asigne una **matriz D3DFORMAT** con el tamaño necesario y llame al método de nuevo. Esta vez, establezca *pFormats* en la dirección de la matriz. El método rellena la matriz con la lista de formatos de píxel.

El controlador debe devolver los formatos en orden decreciente de preferencia, con el formato más preferido en primer lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




