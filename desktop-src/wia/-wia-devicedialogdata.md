---
description: 'Estructura DEVICEDIALOGDATA: define los datos necesarios para llamar a un cuadro de diálogo de dispositivo.'
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Estructura DEVICEDIALOGDATA (Wiadefd.h)
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
ms.openlocfilehash: e20b8689e71031024c46451d3079450061e8112acf1052c12129b89ed9e0a23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451205"
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

Tipo: **HWND**

</dd> <dd>

Especifica el identificador de la ventana primaria del cuadro de diálogo.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***

</dd> <dd>

Apunta a una [**interfaz IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa el elemento raíz válido en el árbol de elementos de aplicación.

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
| CUADRO DE DIÁLOGO \_ DE DISPOSITIVO WIA \_ USO DE LA INTERFAZ DE USUARIO \_ \_ \_ COMÚN | Use la interfaz de usuario del sistema, si está disponible, en lugar de la interfaz de usuario proporcionada por el proveedor. Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor. Si no hay ninguna interfaz de usuario disponible, la función devuelve E \_ NOTIMPL. |



 

</dd> <dt>

**lIntent**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Especifica el tipo de datos que la imagen pretende representar. Para obtener una lista de valores de intención de imagen, vea [**Constantes de intención de imagen**](-wia-imageintentconstants.md).

</dd> <dt>

**lItemCount**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Recibe el número de elementos de la matriz indicado por el **parámetro ppWiaItem.**

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***

</dd> <dd>

Recibe la dirección de una matriz de punteros a [**interfaces IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadefd.h</dt> </dl> |



 

 




