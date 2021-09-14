---
description: Esta tabla temporal habilita la opción de desinstalación de revisión de acción personalizada para las acciones personalizadas agregadas o actualizadas por una revisión.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b6c46ebfcfb82ee23ce6acec998490f53fe67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161489"
---
# <a name="msitransformview"></a>MsiTransformView

Esta tabla temporal habilita la opción [de desinstalación de revisión de](custom-action-patch-uninstall-option.md) acción personalizada para las acciones personalizadas agregadas o actualizadas por una revisión.

Si una revisión agrega o actualiza una acción personalizada con el atributo **msidbCustomActionTypePatchUninstall,** Windows Installer ejecuta la acción personalizada nueva o actualizada cuando se desinstala la revisión. Windows El instalador hace que las actualizaciones dentro de la revisión que se va a desinstalar estén disponibles para la acción personalizada de desinstalación de revisiones. La revisión debe incluir una tabla *&lt; PatchGUID &gt;* de MsiTransformView para proporcionar esta información a Windows Instalador. La información de esta tabla está disponible para cualquier acción personalizada inmediata y no está disponible para las acciones personalizadas diferidas.

**[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite. La [opción de desinstalación de revisión de](custom-action-patch-uninstall-option.md) acción personalizada está disponible a partir Windows Instalador 4.5.

Esta tabla debe denominarse MsiTransformView *&lt; PatchGUID &gt;* Table, donde *&lt; PatchGUID &gt;* es el GUID que identifica de forma única la revisión. La tabla *&lt; PatchGUID &gt;* de MsiTransformView tiene las columnas siguientes.



| Columna  | Tipo                         | Clave | Nullable |
|---------|------------------------------|-----|----------|
| Tabla   | [Identificador](identifier.md) | Y   | No        |
| Columna  | [Texto](text.md)             | Y   | No        |
| Row     | [Texto](text.md)             | Y   | Y        |
| Datos    | [Texto](text.md)             | No   | Y        |
| Current | [Texto](text.md)             | No   | Y        |



 

## <a name="column"></a>Columna

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Mesa
</dt> <dd>

Nombre de una tabla de base de datos modificada.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Columna
</dt> <dd>

Nombre de una columna de tabla modificada o INSERT, DELETE, CREATE o DROP.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Fila
</dt> <dd>

Lista de los valores de clave principal separados por pestañas. Los valores null de clave principal se representan mediante un solo carácter de espacio. Un valor NULL de esta columna indica un cambio de esquema.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Datos
</dt> <dd>

Datos, nombre de un flujo de datos o una definición de columna.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Actual
</dt> <dd>

Valor actual de la base de datos de referencia o columna un número.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las acciones personalizadas de desinstalación de revisiones se ejecutan cuando se desinstala la revisión. No se ejecutan cuando se desinstala el producto. Use la [opción de desinstalación de revisión de](custom-action-patch-uninstall-option.md) acción personalizada y esta tabla para ejecutar un personalizado solo cuando se desinstale la revisión.

Una revisión puede actualizar una acción personalizada proporcionada en el paquete original (.msi archivo). Para ejecutar la versión actualizada de la acción personalizada cuando se desinstale la revisión, marque la acción personalizada con el atributo **msidbCustomActionTypePatchUninstall** en el paquete original.

 

 



