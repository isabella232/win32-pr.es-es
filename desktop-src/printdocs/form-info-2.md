---
description: Contiene información sobre un formulario de impresión traducible.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: Estructura de FORM_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276659"
---
# <a name="form_info_2-structure"></a>Estructura del formulario de \_ información \_ 2

Contiene información sobre un formulario de impresión traducible.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Marcas**
</dt> <dd>

Propiedades del formulario. Se definen los valores siguientes, pero solo se puede establecer uno. Cuando [**GetForm**](getform.md) o [**EnumForms**](enumforms.md)devuelven el **formulario de \_ información \_ 2** , **Flags** se establece en el valor actual de la base de datos de formularios.



| Value         | Significado                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| usuario de formulario \_    | Si se establece esta marca de bits, el formulario lo ha definido el usuario. Los formularios con este marcador se definen en el registro.                                                                                                                                                                    |
| Builtin de formulario \_ | Si se establece esta marca de bits, el formulario forma parte del administrador de trabajos de impresión. Las definiciones de formulario con este marcador establecido no aparecen en el registro. Los formularios integrados no se pueden modificar, por lo que no se debe establecer esta marca cuando la estructura se pasa a [**AddForm**](addform.md) o [**SetForm**](setform.md). |
| impresora de formulario \_ | Si se establece esta marca de bits, el formulario está asociado a una impresora determinada y su definición aparece en el registro.                                                                                                                                                                      |



 

</dd> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del formulario. El nombre del formulario no puede superar los 31 caracteres.

</dd> <dt>

**Tamaño**
</dt> <dd>

Ancho y alto del formulario en milésimas de milímetro.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Ancho y alto, en milésimas de milímetro, del área de la página en la que la impresora puede imprimir.

</dd> <dt>

**pKeyword**
</dt> <dd>

Un puntero a un identificador de cadena no traducible del formulario. Cuando se pasa a [**AddForm**](addform.md) o [**SetForm**](setform.md), proporciona al llamador un medio para identificar el formulario en todas las configuraciones regionales.

</dd> <dt>

**StringType**
</dt> <dd>

Especifica cómo se obtiene un nombre para mostrar localizado del formulario en tiempo de ejecución. Se definen los valores siguientes. Solo se puede establecer una en una llamada determinada a [**AddForm**](addform.md) o [**SetForm**](setform.md). Tanto \_ la cadena MUIDLL como \_ la cadena LANGPAIR se pueden establecer con la **forma \_ info \_ 2** (s) devuelta por [**GetForm**](getform.md) o [**EnumForms**](enumforms.md). Vea la sección Comentarios.



| Value            | Significado                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CADENA \_ None     | No hay ningún nombre para mostrar localizado.                                                                                                                                                            |
| CADENA \_ MUIDLL   | El nombre para mostrar se extrae de la DLL de recursos localizados de la [interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management) especificada en **pMuiDll**. El identificador está en el miembro **dwResourceId** . |
| CADENA \_ LANGPAIR | El nombre para mostrar y el identificador de idioma se proporcionan directamente mediante **pDisplayName** y el idioma lo especifica **wLangId**.                                                                       |



 

</dd> <dt>

**pMuiDll**
</dt> <dd>

La DLL de recursos localizados de la [interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management) que contiene el nombre para mostrar localizado.

</dd> <dt>

**dwResourceId**
</dt> <dd>

El identificador de recurso del nombre para mostrar del formulario en **pMuiDll**.

</dd> <dt>

**pDisplayName**
</dt> <dd>

Nombre para mostrar del formulario en el idioma especificado por **wLangId**.

</dd> <dt>

**wLangId**
</dt> <dd>

El idioma de **pDisplayName**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En una llamada a [**AddForm**](addform.md) o [**SetForm**](setform.md):

-   Si **StringType** es de tipo String \_ None, tanto **pMuiDll** como **pDisplayName** deben ser **null** y **dwResourceId** y **wLangId** deben ser 0.
-   Si **StringType** es de tipo String \_ MUIDLL, **pDisplayName** debe ser **null** y **wLangId** debe ser 0.
-   Si **StringType** es de tipo String \_ LANGPAIR, **pMuiDll** debe ser **null** y **dwResourceId** debe ser 0.

Para un **formulario de \_ información \_ 2** devuelto por una llamada a [**GetForm**](getform.md) o [**EnumForms**](enumforms.md):

-   Si **StringType** es tanto String \_ MUIDLL como String \_ LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId** y **wLangId** tendrán valores válidos.
-   Si **StringType** es de tipo cadena \_ MUIDLL, **pMuiDll** y **dwResourceId** tendrán valores válidos. **pDisplayName** será **null** y **wLangId** será 0.
-   Si **StringType** es de tipo cadena \_ LANGPAIR, **pDisplayName** y **wLangId** tendrán valores válidos. **pMuiDll** será **null** y **dwResourceId** será 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Form \_ info \_ 2W** (Unicode) y **\_ Form \_ info \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[Interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

