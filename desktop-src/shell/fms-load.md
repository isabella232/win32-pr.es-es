---
description: Contiene información que el Administrador de archivos usa para agregar un menú personalizado proporcionado por un archivo DLL de extensión del Administrador de archivos. La estructura también proporciona un valor delta que el archivo DLL de extensión puede usar para manipular el menú personalizado después de que el Administrador de archivos haya cargado el menú.
title: FMS_LOAD estructura (Wfext.h)
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
ms.openlocfilehash: 8c2c2d476281c50f19d73c8af1572e1c2d8430149d8664efe14f0d5042c00542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032653"
---
# <a name="fms_load-structure"></a>Estructura \_ DE FMS LOAD

Contiene información que el Administrador de archivos usa para agregar un menú personalizado proporcionado por un archivo DLL de extensión del Administrador de archivos. La estructura también proporciona un valor delta que el archivo DLL de extensión puede usar para manipular el menú personalizado después de que el Administrador de archivos haya cargado el menú.

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

Longitud, en bytes, de la estructura .

</dd> <dt>

**szMenuName**
</dt> <dd>

Tipo: **\[ LEN \_ \_ \] DE TEXTO DEL MENÚ TCHAR**

</dd> <dd>

Nombre terminado en NULL para un elemento de menú que aparece en la barra de menús del Administrador de archivos.

</dd> <dt>

**hMenu**
</dt> <dd>

Tipo: **HMENU**

</dd> <dd>

Identificador del menú emergente agregado a la barra de menús del Administrador de archivos.

</dd> <dt>

**wMenuDelta**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Valor delta del elemento de menú. Para evitar conflictos con sus propios elementos de menú, el Administrador de archivos vuelve a numerar los identificadores de elemento de menú en el menú emergente identificado por el **miembro hMenu** agregando este valor diferencial a cada identificador. Un archivo DLL de extensión que debe modificar un elemento de menú debe identificar el elemento agregando el valor delta al identificador del elemento de menú. El valor de este miembro puede variar de una sesión a otra.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




