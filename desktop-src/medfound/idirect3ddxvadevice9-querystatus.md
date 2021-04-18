---
description: Consulta el estado de lectura y escritura de una superficie de descodificación de aceleración de vídeo de DirectX (DXVA).
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'IDirect3DDXVADevice9:: QueryStatus (método) (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715441"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a>IDirect3DDXVADevice9:: QueryStatus (método)

Consulta el estado de lectura y escritura de una superficie de descodificación de aceleración de vídeo de DirectX (DXVA).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSurface* 
</dt> <dd>

Puntero a la interfaz **IDirect3DSurface9** de la superficie que se va a consultar.

</dd> <dt>

*Marcas* 
</dt> <dd>

Especifica el tipo de consulta que se va a realizar.



| Value                                                                                                                             | Significado                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <dt>**0x00**</dt> </dl> | Compruebe si la superficie es segura para su uso en la escritura.<br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <dt>**0x01**</dt> </dl> | Compruebe si la superficie se usa con seguridad para la lectura.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




