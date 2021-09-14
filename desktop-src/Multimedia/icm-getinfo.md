---
title: ICM_GETINFO mensaje (Vfw.h)
description: El ICM getinfo consulta un controlador de compresión de vídeo para devolver una descripción de sí \_ mismo en una estructura ICINFO.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246261"
---
# <a name="icm_getinfo-message"></a>\_ICM Mensaje GETINFO

El **ICM \_ getinfo** consulta un controlador de compresión de vídeo para devolver una descripción de sí mismo en una [**estructura ICINFO.**](/windows/desktop/api/Vfw/ns-vfw-icinfo)


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*
</dt> <dd>

Puntero a una **estructura ICINFO** para contener información.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamaño, en bytes, de **ICINFO**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tamaño, en bytes, de [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) o cero si se produce un error.

## <a name="remarks"></a>Observaciones

Normalmente, las aplicaciones envían este mensaje para mostrar una lista de los dispositivos instalados.

El controlador debe rellenar todos los miembros de la [**estructura ICINFO,**](/windows/desktop/api/Vfw/ns-vfw-icinfo) excepto **szDriver**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensajes de compresión de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





