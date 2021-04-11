---
description: Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: Estructura DEVICEDIALOGDATA2 (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: f4ab56114054b4f69a21fd9f4c05a1e119bab5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082673"
---
# <a name="devicedialogdata2-structure"></a>Estructura DEVICEDIALOGDATA2

Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica el tamaño de esta estructura en bytes.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

</dd> <dd>

Apunta a una interfaz [_ *IWiaItem2* *](-wia-iwiaitem2.md) que representa el elemento raíz válido en el árbol de elementos de la aplicación.

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica un conjunto de marcas que controlan la operación del cuadro de diálogo. Se puede establecer en cualquiera de los siguientes valores:



| Marca                                 | Significado                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamiento predeterminado.                                                                                                                                                                           |
| \_cuadro de diálogo de dispositivo WIA \_ \_ \_ imagen única   | Restrinja la selección de imágenes a una sola imagen en el cuadro de diálogo adquisición de imagen de dispositivo.                                                                                                      |
| cuadro de diálogo de dispositivo WIA uso de la \_ \_ interfaz de \_ \_ \_ usuario común | Use la interfaz de usuario del sistema, si está disponible, en lugar de la interfaz de usuario proporcionada por el proveedor. Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor. Si no hay ninguna interfaz de usuario disponible, la función devuelve E \_ NOTIMPL. |



 

</dd> <dt>

**hwndParent**
</dt> <dd>

Tipo: **hWnd**

</dd> <dd>

Especifica el identificador de la ventana primaria del cuadro de diálogo.

</dd> <dt>

**bstrFolderName**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Especifica el nombre de la carpeta donde se transfieren los archivos.

</dd> <dt>

**bstrFilename**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Especifica la plantilla de nombre de archivo que se va a usar para los archivos transferidos desde elementos WIA a la carpeta de destino designada por **bstrFolderName**. Se puede crear un número arbitrario de nombres de archivo únicos anexando caracteres adicionales a la plantilla de nombre de archivo.

</dd> <dt>

**lNumFiles**
</dt> <dd>

Tipo: **Long**

</dd> <dd>

Recibe el número de cadenas escritas en la matriz **pbstrFilePaths** .

</dd> <dt>

**pbstrFilePaths**
</dt> <dd>

Tipo: **BSTR \** _

</dd> <dd>

Puntero a una matriz de punteros BSTR. Cada elemento de la matriz apunta a un BSTR que contiene el nombre de destino de un archivo que se ha transferido correctamente a la carpeta identificada por bstrFolderName. El método debe asignar el almacenamiento de este miembro.

</dd> <dt>

_ *ppWiaItem**
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

</dd> <dd>

Puntero a la interfaz [_ *IWiaItem2* *](-wia-iwiaitem2.md) del elemento WIA que transfiere los datos al archivo o los archivos nombrados en la matriz **pbstrFilePaths** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadefd. h</dt> </dl> |



 

 




