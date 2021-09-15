---
description: Consulta la cantidad de memoria cero que asignará la capa de abstracción de hardware (RASP) para su uso privado.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: Método IDirect3DVideoDevice9::GetDXVAInternalInfo (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579988"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a>IDirect3DVideoDevice9::GetDXVAInternalInfo (método)

Consulta la cantidad de memoria cero que asignará la capa de abstracción de hardware (RASP) para su uso privado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGuid* 
</dt> <dd>

Puntero a un GUID que especifica el perfil dxva. Para obtener una lista de perfiles admitidos, llame a [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pUncompData* 
</dt> <dd>

Puntero a una [**estructura DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica el tamaño y el formato de píxel de los datos sin comprimir.

</dd> <dt>

*pMemoryUsed* 
</dt> <dd>

Recibe la cantidad de memoria de cero que asignará LAN, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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

 

 




