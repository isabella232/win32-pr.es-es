---
description: Define el comportamiento de la solicitud del almacén protegido cada vez que muestra una interfaz de usuario.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: PST_PROMPTINFO estructura (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670839"
---
# <a name="pst_promptinfo-structure"></a>\_Estructura PROMPTINFO de PST

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Define el comportamiento de la solicitud del almacén protegido cada vez que muestra una interfaz de usuario.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de esta estructura.

</dd> <dt>

**dwPromptFlags**
</dt> <dd>

Esta marca se omite.



| Value                                                                                                                                                                                                                                          | Significado                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <dt>**Archivo pst \_ PF \_ siempre \_ muestra**</dt> <dt>0x00000001</dt> </dl> | Solicita que el proveedor muestre el cuadro de diálogo de solicitud al usuario, incluso si no es necesario para este acceso. <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <dt>**Archivo pst \_ PF \_ nunca \_ muestra**</dt> <dt>0x00000002</dt> </dl>    | No muestre el cuadro de diálogo de solicitud al usuario.<br/>                                                                 |



 

</dd> <dt>

**hwndApp**
</dt> <dd>

Identificador de la ventana primaria de la interfaz de usuario. El miembro **hwndApp** determina dónde aparece la interfaz de usuario. Si se pasa **null** , se considera que el escritorio es la ventana primaria.

</dd> <dt>

**szPrompt**
</dt> <dd>

La cadena de solicitud.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeleteItem**](ipstore-deleteitem.md)
</dt> <dt>

[**OpenItem**](ipstore-openitem.md)
</dt> <dt>

[**ReadItem**](ipstore-readitem.md)
</dt> <dt>

[**WriteItem**](ipstore-writeitem.md)
</dt> </dl>

 

 
