---
description: Esta tabla temporal habilita la opción de desinstalación de revisiones de acción personalizada para las acciones personalizadas agregadas o actualizadas por una revisión.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978f27fe68d89abd3ea94a4d13adc815bbc6510564caf949b937d8a4213428b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944253"
---
# <a name="msitransformview"></a>MsiTransformView

Esta tabla temporal habilita la opción [de desinstalación de revisiones de](custom-action-patch-uninstall-option.md) acción personalizada para las acciones personalizadas agregadas o actualizadas por una revisión.

Si una revisión agrega o actualiza una acción personalizada con el atributo **msidbCustomActionTypePatchUninstall,** el instalador de Windows ejecuta la acción personalizada nueva o actualizada cuando se desinstala la revisión. Windows El instalador hace que las actualizaciones de la revisión que se va a desinstalar estén disponibles para la acción personalizada de desinstalación de revisiones. La revisión debe incluir una tabla MsiTransformView *<PatchGUID>* para proporcionar esta información a Windows Installer. La información de esta tabla está disponible para cualquier acción personalizada inmediata y no está disponible para las acciones personalizadas diferidas.

**[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite. La [opción de desinstalación de revisiones de acción personalizada](custom-action-patch-uninstall-option.md) está disponible a partir de Windows Installer 4.5.

Esta tabla debe denominarse MsiTransformView *<PatchGUID>* Table, donde *<PatchGUID>* es el GUID que identifica de forma única la revisión. La tabla MsiTransformView *<PatchGUID>* tiene las columnas siguientes.



| Columna  | Tipo                         | Clave | Nullable |
|---------|------------------------------|-----|----------|
| Tabla   | [Identificador](identifier.md) | Y   | N        |
| Columna  | [Texto](text.md)             | Y   | N        |
| Fila     | [Texto](text.md)             | Y   | Y        |
| Datos    | [Texto](text.md)             | N   | Y        |
| Current | [Texto](text.md)             | N   | Y        |



 

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

## <a name="remarks"></a>Comentarios

Las acciones personalizadas de desinstalación de revisiones se ejecutan cuando se desinstala la revisión. No se ejecutan cuando se desinstala el producto. Use la [opción Desinstale revisión de acciones personalizadas](custom-action-patch-uninstall-option.md) y esta tabla para ejecutar un personalizado solo cuando se desinstale la revisión.

Una revisión puede actualizar una acción personalizada proporcionada en el paquete original (.msi archivo). Para ejecutar la versión actualizada de la acción personalizada cuando se desinstale la revisión, marque la acción personalizada con el atributo **msidbCustomActionTypePatchUninstall** en el paquete original.

 

 



