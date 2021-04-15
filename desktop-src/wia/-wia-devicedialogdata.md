---
description: Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Estructura DEVICEDIALOGDATA (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545566"
---
# <a name="devicedialogdata-structure"></a>Estructura DEVICEDIALOGDATA

Define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica el tamaño de esta estructura en bytes.

</dd> <dt>

**hwndParent**
</dt> <dd>

Tipo: **hWnd**

</dd> <dd>

Especifica el identificador de la ventana primaria del cuadro de diálogo.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _

</dd> <dd>

Apunta a una interfaz [_ *IWiaItem* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa el elemento raíz válido en el árbol de elementos de la aplicación.

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

**lIntent**
</dt> <dd>

Tipo: **Long**

</dd> <dd>

Especifica el tipo de datos que va a representar la imagen. Para obtener una lista de valores de intención de imagen, vea [**constantes de intención de imagen**](-wia-imageintentconstants.md).

</dd> <dt>

**lItemCount**
</dt> <dd>

Tipo: **Long**

</dd> <dd>

Recibe el número de elementos de la matriz indicado por el parámetro **ppWiaItem** .

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***

</dd> <dd>

Recibe la dirección de una matriz de punteros a las interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wiadefd. h</dt> </dl> |



 

 




