---
title: Estructura WMDMMetadataView
description: La estructura WMDMMetadataView define la vista de metadatos. El contenido se organiza en función de esta definición.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Estructura WMDMMetadataView Administrador de dispositivos Windows Media
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698557"
---
# <a name="wmdmmetadataview-structure"></a>Estructura WMDMMetadataView

La estructura **WMDMMetadataView** define la vista de metadatos. El contenido se organiza en función de esta definición.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pwszViewName**
</dt> <dd>

Puntero a una cadena de caracteres anchos terminada en null que contiene el nombre de la vista. Se utiliza como el nombre del nodo raíz en el que se presenta esta vista.

</dd> <dt>

**nDepth**
</dt> <dd>

Entero que contiene la profundidad de la vista, que indica el número de etiquetas de metadatos anidadas que se utilizan para la vista.

</dd> <dt>

**ppwszTags**
</dt> <dd>

Matriz de cadenas de etiquetas de metadatos para las etiquetas anidadas.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el código siguiente se crea una vista de metadatos:


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



El código anterior organiza el contenido de la manera siguiente:

<dl> Mi vista<dl> Genre1<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





