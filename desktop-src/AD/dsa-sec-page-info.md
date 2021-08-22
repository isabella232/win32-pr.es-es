---
title: DSA_SEC_PAGE_INFO estructura
description: Se usa con los mensajes WM ADSPROP SHEET CREATE y WM DSA SHEET CREATE NOTIFY para definir una hoja de propiedades secundaria en Active Directory \_ \_ complemento \_ \_ \_ \_ \_ MMC.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO estructura Active Directory
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
ms.openlocfilehash: 26fa3dcfb983de8e1052b319bac7c3a594e256b594847c32b553353e6caee17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695653"
---
# <a name="dsa_sec_page_info-structure"></a>Estructura DE INFORMACIÓN DE PÁGINA de DSA \_ SEC \_ \_

La estructura **DSA \_ SEC \_ PAGE \_ INFO** se usa con los mensajes [**WM \_ ADSPROP SHEET \_ \_ CREATE**](wm-adsprop-sheet-create.md) y [**WM \_ DSA \_ SHEET CREATE \_ \_ NOTIFY**](wm-dsa-sheet-create-notify.md) para definir una hoja de propiedades secundaria en un complemento MMC de Active Directory.

> [!Note]  
> Esta estructura no se define en un archivo de encabezado publicado. Para usar esta estructura, defón quieres definirla en el formato exacto que se muestra.

 

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

Contiene el desplazamiento, en bytes, desde el inicio de la estructura PAGE INFO de **DSA \_ SEC \_ \_** a una cadena Unicode terminada en NULL que contiene el título de la hoja de propiedades secundaria.

</dd> <dt>

**dsObjectNames**
</dt> <dd>

Contiene una [**estructura DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) que define la hoja de propiedades secundaria. Solo se puede crear una hoja de propiedades secundaria a la vez, por lo que la estructura **DSOBJECTNAMES** solo puede contener una [**estructura DSOBJECT.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**WM \_ ADSPROP \_ SHEET \_ CREATE**](wm-adsprop-sheet-create.md)
</dt> <dt>

[**WM \_ DSA \_ SHEET \_ CREATE \_ NOTIFY**](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





