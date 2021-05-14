---
description: Contiene información sobre los botones personalizados que se van a agregar a la barra de herramientas del Administrador de archivos. Los botones los proporciona un archivo DLL de extensión del Administrador de archivos.
title: FMS_TOOLBARLOAD estructura (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 3a993312b9e365561018459c43dab87afbd3c2b2
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842166"
---
# <a name="fms_toolbarload-structure"></a>ESTRUCTURA FMS \_ TOOLBARLOAD

Contiene información sobre los botones personalizados que se van a agregar a la barra de herramientas del Administrador de archivos. Los botones los proporciona un archivo DLL de extensión del Administrador de archivos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a>Members

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño, en bytes, de la estructura . El Administrador de archivos establece el tamaño antes de llamar a la extensión y comprueba el tamaño después de que se devuelva el procedimiento de extensión.

</dd> <dt>

**lpButtons**
</dt> <dd>

Tipo: **LPEXT \_ BUTTON**

</dd> <dd>

Dirección de una matriz de [**estructuras EXT \_ BUTTON.**](ext-button.md)

</dd> <dt>

**cButtons**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de estructuras [**EXT \_ BUTTON**](ext-button.md) de la matriz a la que apunta **el miembro lpButtons.** Este número es igual al número de botones y separadores que se agregarán a la barra de herramientas.

</dd> <dt>

**cBitmaps**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Número de botones representados por el mapa de bits especificado.

</dd> <dt>

**idBitmap**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Identificador de un recurso de mapa de bits en el archivo ejecutable para el archivo DLL de extensión. El recurso de mapa de bits contiene imágenes para el número de botones especificado por **cBitmaps.** El Administrador de archivos carga el recurso de mapa de bits y, a continuación, lo usa para mostrar los botones.

</dd> <dt>

**hBitmap**
</dt> <dd>

Tipo: **HBITMAP**

</dd> <dd>

Identificador de un mapa de bits que el Administrador de archivos usará para obtener y mostrar imágenes de botón si **idBitmap** es 0.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> </dl>

 

 




