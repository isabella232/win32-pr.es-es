---
description: Obtiene información sobre los búferes comprimidos necesarios para la decodización acelerada por hardware.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: Método IDirect3DVideoDevice9::GetDXVACompressedBufferInfo (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: efb96ec457cdb81f89982947bf1b9bc40543789b2e9ac253d83c81727f1efae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942295"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a>IDirect3DVideoDevice9::GetDXVACompressedBufferInfo (método)

Obtiene información sobre los búferes comprimidos necesarios para la decodización acelerada por hardware.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
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

*pNumBuffers* 
</dt> <dd>

En la entrada, especifica el número de elementos de la matriz *pBufferInfo.* Si *pBufferInfo* es **NULL,** el valor de `*pNumBuffers` debe ser cero.

En la salida, si *pBufferInfo* es **NULL,** *pNumBuffers* recibe el tamaño de la matriz que se va a asignar. De lo contrario, *pNumBuffers* recibe el número real de elementos que se copian en la matriz *pBufferInfo.*

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Dirección de una matriz [**de estructuras DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) o **NULL.** Si el valor no es **NULL,** el método copia una lista de **estructuras DXVACompBufferInfo** en esta matriz. Cada estructura corresponde a un tipo de búfer de datos comprimidos que usa el acelerador de vídeo.

Establezca todos los elementos de la matriz en cero antes de llamar a este método.

Cada índice de matriz corresponde a uno de los tipos de superficie DXVA definidos en dxva.h. El acelerador de vídeo devuelve una lista de hasta entradas de la matriz **DXVA \_ NUM TYPES \_ COMP \_ \_ BUFFERS.** Para obtener más información, consulte la especificación [DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration), sección 3.4, "Lista de descripción del búfer". Si el perfil de DXVA no usa un tipo de búfer determinado, la entrada de ese índice contiene ceros para todos los valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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

 

 
