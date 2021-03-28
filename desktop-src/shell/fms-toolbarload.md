---
description: Contiene información acerca de los botones personalizados que se van a agregar a la barra de herramientas del administrador de archivos. Los botones los proporciona un archivo DLL de extensión del administrador de archivos.
title: FMS_TOOLBARLOAD estructura (Wfext. h)
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
ms.openlocfilehash: 8e123c759a827adddf5fd00eaf33193ebca0dbf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985507"
---
# <a name="fms_toolbarload-structure"></a>Estructura de FMS \_ TOOLBARLOAD

Contiene información acerca de los botones personalizados que se van a agregar a la barra de herramientas del administrador de archivos. Los botones los proporciona un archivo DLL de extensión del administrador de archivos.

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



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño de la estructura, en bytes. El administrador de archivos establece el tamaño antes de llamar a la extensión y comprueba el tamaño después de que el procedimiento de extensión se devuelva.

</dd> <dt>

**lpButtons**
</dt> <dd>

Escriba: **\_ botón LPEXT**

</dd> <dd>

Dirección de una matriz de estructuras [**de \_ botones ext**](ext-button.md) .

</dd> <dt>

**cButtons**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

El número de estructuras de [**\_ botón ext**](ext-button.md) en la matriz a la que señala el miembro **lpButtons** . Este número es igual al número de botones y separadores que se van a agregar a la barra de herramientas.

</dd> <dt>

**cBitmaps**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Número de botones que representa el mapa de bits especificado.

</dd> <dt>

**idBitmap**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Identificador de un recurso de mapa de bits en el archivo ejecutable para el archivo DLL de extensión. El recurso de mapa de bits contiene imágenes para el número de botones especificado por **cBitmaps**. El administrador de archivos carga el recurso de mapa de bits y, a continuación, lo usa para mostrar los botones.

</dd> <dt>

**hBitmap**
</dt> <dd>

Tipo: **hBitmap**

</dd> <dd>

Identificador de un mapa de bits que el administrador de archivos usará para obtener y mostrar imágenes de botón si **idBitmap** es 0.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> </dl>

 

 




