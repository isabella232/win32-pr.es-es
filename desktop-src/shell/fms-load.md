---
description: Contiene información que utiliza el administrador de archivos para agregar un menú personalizado proporcionado por un archivo DLL de extensión del administrador de archivos. La estructura también proporciona un valor Delta que el archivo DLL de extensión puede utilizar para manipular el menú personalizado una vez que el administrador de archivos ha cargado el menú.
title: FMS_LOAD estructura (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: 1745c4e34ac124e9990602350db6479ce287be8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984203"
---
# <a name="fms_load-structure"></a>Estructura de carga de FMS \_

Contiene información que utiliza el administrador de archivos para agregar un menú personalizado proporcionado por un archivo DLL de extensión del administrador de archivos. La estructura también proporciona un valor Delta que el archivo DLL de extensión puede utilizar para manipular el menú personalizado una vez que el administrador de archivos ha cargado el menú.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Longitud, en bytes, de la estructura.

</dd> <dt>

**szMenuName**
</dt> <dd>

Tipo: **\[ texto del menú TCHAR \_ \_ longitud \]**

</dd> <dd>

Un nombre terminado en null para un elemento de menú que aparece en la barra de menús del administrador de archivos.

</dd> <dt>

**hMenu**
</dt> <dd>

Tipo: **HMENU**

</dd> <dd>

Identificador del menú emergente que se ha agregado a la barra de menús del administrador de archivos.

</dd> <dt>

**wMenuDelta**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Valor Delta del elemento de menú. Para evitar conflictos con sus propios elementos de menú, el administrador de archivos renumera los identificadores de elemento de menú en el menú emergente identificado por el miembro **hMenu** agregando este valor Delta a cada identificador. Un archivo DLL de extensión que debe modificar un elemento de menú debe identificar el elemento agregando el valor delta al identificador del elemento de menú. El valor de este miembro puede variar de una sesión a una sesión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




