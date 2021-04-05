---
title: Estructura de DSA_SEC_PAGE_INFO
description: Se usa con la \_ hoja de ADSPROP de WM \_ \_ creación y la \_ hoja DSA de WM creación de mensajes de \_ \_ \_ notificación para definir una hoja de propiedades secundaria en un complemento de MMC de Active Directory.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- Estructura de DSA_SEC_PAGE_INFO Active Directory
- PDSA_SEC_PAGE_INFO puntero de estructura Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996656"
---
# <a name="dsa_sec_page_info-structure"></a>\_Estructura de \_ información de página DSA s \_

La estructura de información de la **\_ \_ página \_ DSA sec** se usa con la hoja de [**ADSPROP de WM \_ \_ \_ creación**](wm-adsprop-sheet-create.md) y la hoja de DSA de WM creación de mensajes de [**\_ \_ \_ \_ notificación**](wm-dsa-sheet-create-notify.md) para definir una hoja de propiedades secundaria en un complemento MMC de Active Directory.

> [!Note]  
> Esta estructura no está definida en un archivo de encabezado publicado. Para usar esta estructura, debe definirla en el formato exacto que se muestra.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**hwndParentSheet**
</dt> <dd>

Contiene el identificador de ventana del elemento primario de la hoja de propiedades secundaria.

</dd> <dt>

**offsetTitle**
</dt> <dd>

Contiene el desplazamiento, en bytes, desde el inicio de la estructura de **\_ información de \_ página \_ de DSA s** hasta una cadena Unicode terminada en null que contiene el título de la hoja de propiedades secundaria.

</dd> <dt>

**dsObjectNames**
</dt> <dd>

Contiene una estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) que define la hoja de propiedades secundaria. Solo se puede crear una hoja de propiedades secundaria a la vez, por lo que la estructura **DSOBJECTNAMES** solo puede contener una estructura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**hoja de ADSPROP de WM \_ \_ \_ creación**](wm-adsprop-sheet-create.md)
</dt> <dt>

[**\_ \_ \_ crear notificación de la hoja DSA de WM \_**](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





