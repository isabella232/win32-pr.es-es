---
description: La estructura FORM_INFO_1 contiene información sobre un formulario de impresión. La información incluye el origen de los formularios de impresión, su nombre, sus dimensiones y las dimensiones de su área imprimible.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: Estructura de FORM_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720592"
---
# <a name="form_info_1-structure"></a>Estructura de FORM_INFO_1

La estructura **FORM_INFO_1** contiene información sobre un formulario de impresión. La información incluye el origen del formulario de impresión, su nombre, sus dimensiones y las dimensiones de su área imprimible.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Marcas**
</dt> <dd>

Propiedades del formulario. Se definen los valores siguientes.



| Value         | Significado                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| FORM_USER    | Si se establece esta marca de bits, el formulario lo ha definido el usuario. Los formularios con este marcador se definen en el registro.        |
| FORM_BUILTIN | Si se establece esta marca de bits, el formulario forma parte del administrador de trabajos de impresión. Las definiciones de formulario con este marcador establecido no aparecen en el registro. |
| FORM_PRINTER | Si se establece esta marca de bits, el formulario está asociado a una impresora determinada y su definición aparece en el registro.          |



 

</dd> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del formulario. El nombre del formulario no puede superar los 31 caracteres.

</dd> <dt>

**Tamaño**
</dt> <dd>

Ancho y alto, en milésimas de milímetro, del formulario.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Ancho y alto, en milésimas de milímetro, del formulario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **_FORM_INFO_1W** (Unicode) y **_FORM_INFO_1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

 




