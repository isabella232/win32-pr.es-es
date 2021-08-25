---
title: WMDMMetadataView (estructura)
description: La estructura WMDMMetadataView define la vista de metadatos. El contenido se organiza en función de esta definición.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Estructura WMDMMetadataView windows Media Administrador de dispositivos
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
ms.openlocfilehash: 8e442ed3058f1982ac7607c6b8a29e5df321d69776695821b278049e27cd7589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862595"
---
# <a name="wmdmmetadataview-structure"></a>WMDMMetadataView (estructura)

La **estructura WMDMMetadataView** define la vista de metadatos. El contenido se organiza en función de esta definición.

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

Puntero a una cadena terminada en null de caracteres anchos que contiene el nombre de la vista. Se usa como nombre del nodo raíz bajo el que se presenta esta vista.

</dd> <dt>

**nDepth**
</dt> <dd>

Entero que contiene la profundidad de la vista, que indica cuántas etiquetas de metadatos anidados se usan para la vista.

</dd> <dt>

**ppwszTags**
</dt> <dd>

Matriz de cadenas de etiquetas de metadatos para las etiquetas anidadas.

</dd> </dl>

## <a name="examples"></a>Ejemplos

El código siguiente crea una vista de metadatos:


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



El código anterior organiza el contenido de la siguiente manera:

<dl> Mi vista<dl> Genre1<dl> Artist1<dl> Album1<dl> Canción1  
Canción 2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Canción1  
Canción 2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> Artist1<dl> Album1<dl> Canción1  
Canción 2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Canción1  
Canción 2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





