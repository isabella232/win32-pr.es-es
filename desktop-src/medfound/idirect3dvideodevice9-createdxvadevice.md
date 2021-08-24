---
description: Crea un dispositivo descodificador de aceleración de vídeo de DirectX (DXVA).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: Método IDirect3DVideoDevice9::CreateDXVADevice (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 4f70f976487db270145c8587107499f3c4e84ad85dacf99bec21050a2684b723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555735"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a>IDirect3DVideoDevice9::CreateDXVADevice (Método)

Crea un dispositivo descodificador de aceleración de vídeo de DirectX (DXVA).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGuid* 
</dt> <dd>

Puntero a un GUID que especifica el dispositivo que se creará.

</dd> <dt>

*pUncompData* 
</dt> <dd>

Puntero a [**una estructura DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica el formato de la imagen sin comprimir.

</dd> <dt>

*pData* 
</dt> <dd>

Puntero a una **estructura \_ ConnectMode de DXVA** que especifica el modo DXVA y el perfil restringido.

</dd> <dt>

*DataSize* 
</dt> <dd>

Tamaño de la **estructura \_ ConnectMode de DXVA,** en bytes.

</dd> <dt>

*ppDXVADevice* 
</dt> <dd>

Recibe un puntero a la [**interfaz IDirect3DDXVADevice9.**](idirect3ddxvadevice9.md) El autor de la llamada debe liberar la interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




