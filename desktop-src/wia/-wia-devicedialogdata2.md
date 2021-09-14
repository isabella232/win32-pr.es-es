---
description: 'Estructura DEVICEDIALOGDATA2: define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.'
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: Estructura DEVICEDIALOGDATA2 (Wiadefd.h)
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
ms.openlocfilehash: 82ca6cba81101e577eed882ad45272ab81546fed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262348"
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



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica el tamaño de esta estructura en bytes.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

</dd> <dd>

Apunta a una [**interfaz IWiaItem2**](-wia-iwiaitem2.md) que representa el elemento raíz válido en el árbol de elementos de aplicación.

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica un conjunto de marcas que controlan la operación del cuadro de diálogo. Se puede establecer en cualquiera de los valores siguientes:



| Marca                                 | Significado                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamiento predeterminado.                                                                                                                                                                           |
| IMAGEN ÚNICA \_ DEL CUADRO DE DIÁLOGO DE DISPOSITIVO \_ \_ \_ WIA   | Restrinja la selección de imágenes a una sola imagen en el cuadro de diálogo de adquisición de imágenes del dispositivo.                                                                                                      |
| CUADRO DE DIÁLOGO \_ DE DISPOSITIVO WIA \_ USAR INTERFAZ DE USUARIO \_ \_ \_ COMÚN | Use la interfaz de usuario del sistema, si está disponible, en lugar de la interfaz de usuario proporcionada por el proveedor. Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor. Si ninguna interfaz de usuario está disponible, la función devuelve E \_ NOTIMPL. |



 

</dd> <dt>

**hwndParent**
</dt> <dd>

Tipo: **HWND**

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

Especifica la plantilla de nombre de archivo que se va a usar para los archivos transferidos de elementos WIA a la carpeta de destino designada **por bstrFolderName**. Se puede crear un número arbitrario de nombres de archivo únicos anexando caracteres adicionales a la plantilla de nombre de archivo.

</dd> <dt>

**lNumFiles**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Recibe el número de cadenas escritas en la **matriz pbstrFilePaths.**

</dd> <dt>

**pbstrFilePaths**
</dt> <dd>

Tipo: **BSTR \***

</dd> <dd>

Puntero a una matriz de punteros BSTR. Cada elemento de matriz apunta a un BSTR que contiene el nombre de destino de un archivo que se ha transferido correctamente a la carpeta identificada por bstrFolderName. El método debe asignar el almacenamiento para este miembro.

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

</dd> <dd>

Puntero a la [**interfaz IWiaItem2**](-wia-iwiaitem2.md) del elemento WIA que transfiere datos al archivo o archivos denominados en la matriz **pbstrFilePaths.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadefd.h</dt> </dl> |



 

 




