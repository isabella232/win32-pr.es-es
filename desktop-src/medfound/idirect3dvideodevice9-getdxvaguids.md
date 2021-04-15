---
description: Obtiene una lista de perfiles de aceleración de vídeo de DirectX (DXVA) admitidos por el controlador de pantalla.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'IDirect3DVideoDevice9:: GetDXVAGuids (método) (DXVA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715884"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a>IDirect3DVideoDevice9:: GetDXVAGuids (método)

Obtiene una lista de perfiles de aceleración de vídeo de DirectX (DXVA) admitidos por el controlador de pantalla.

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

En la entrada, especifica el número de elementos de la matriz *pGuids* . Si *pGuids* es **null**, el valor de `*pNumGuids` debe ser cero.

En la salida, si *pGuids* es **null**, *pNumGuids* recibe el número de perfiles de DXVA en modo restringido. De lo contrario, *pNumGuids* recibe el número real de GUID que se copian en la matriz *pGuids* .

</dd> <dt>

*pGuids* 
</dt> <dd>

Dirección de una matriz de GUID o **null**. Si el valor no es **null**, la matriz recibe una lista de GUID que especifican los perfiles de DXVA en modo restringido. Estos GUID se definen en DXVA. h y se documentan en la [especificación de dxva 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Llame a este método dos veces. En la primera llamada, establezca *pGuids* en **null**. El parámetro *pNumGuids* recibe el número de GUID de Perfil de DXVA. Asigne una matriz de GUID con el tamaño necesario y vuelva a llamar al método. Esta vez, establezca *pGuids* en la dirección de la matriz. El método rellena la matriz con la lista de GUID de Perfil de DXVA.

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

 

 
