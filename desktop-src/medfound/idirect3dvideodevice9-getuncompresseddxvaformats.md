---
description: Obtiene una lista de formatos de píxeles sin comprimir que se pueden representar con un perfil de aceleración de vídeo de DirectX (DXVA) especificado.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'IDirect3DVideoDevice9:: GetUncompressedDXVAFormats (método) (DXVA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360614"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a>IDirect3DVideoDevice9:: GetUncompressedDXVAFormats (método)

Obtiene una lista de formatos de píxeles sin comprimir que se pueden representar con un perfil de aceleración de vídeo de DirectX (DXVA) especificado.

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

Puntero a un GUID que especifica el perfil de DXVA. Para obtener una lista de los perfiles compatibles, llame a [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pNumFormats* 
</dt> <dd>

En la entrada, especifica el número de elementos de la matriz *pFormats* . Si *pFormats* es **null**, el valor de `*pNumFormats` debe ser cero.

En la salida, si *pFormats* es **null**, *pNumFormats* recibe el número de formatos de píxel admitidos. De lo contrario, *pNumFormats* recibe el número real de formatos de píxel copiados en la matriz *pFormats* .

</dd> <dt>

*pFormats* 
</dt> <dd>

Dirección de una matriz de valores **D3DFORMAT** o **null**. Si el valor no es **null**, la matriz recibe una lista de formatos de píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Llame a este método dos veces. En la primera llamada, establezca *pFormats* en **null**. El parámetro *pNumFormats* recibe el número de formatos. Asigne una matriz **D3DFORMAT** con el tamaño necesario y vuelva a llamar al método. Esta vez, establezca *pFormats* en la dirección de la matriz. El método rellena la matriz con la lista de formatos de píxeles.

El controlador debe devolver los formatos en orden decreciente de preferencia, con el formato más preferido indicado en primer lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




