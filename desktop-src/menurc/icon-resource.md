---
title: Recurso de icono
description: Define un mapa de bits que define la forma del icono que se va a utilizar para una aplicación determinada o un Icono animado.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- Menús de recursos de icono y otros recursos
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533118"
---
# <a name="icon-resource"></a>Recurso de icono

Define un mapa de bits que define la forma del icono que se va a utilizar para una aplicación determinada o un Icono animado.

``` syntax
nameID ICON filename
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nombre único o un valor entero sin signo de 16 bits que identifica el recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extensión*
</dt> <dd>

Nombre del archivo que contiene el recurso. El nombre debe ser un nombre de archivo válido. debe ser una ruta de acceso completa si el archivo no está en el directorio de trabajo actual. La ruta de acceso debe ser una cadena entre comillas.

</dd> </dl>

Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores. Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).

## <a name="remarks"></a>Observaciones

Los recursos de icono y cursor pueden contener más de una imagen.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se definen dos recursos de icono:

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Usar iconos](./using-icons.md)
</dt> </dl>

 

 