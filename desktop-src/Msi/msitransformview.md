---
description: Esta tabla temporal habilita la opción de desinstalación de revisión de acción personalizada para las acciones personalizadas agregadas o actualizadas por una revisión.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678247"
---
# <a name="msitransformview"></a>MsiTransformView

Esta tabla temporal habilita la [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) para las acciones personalizadas agregadas o actualizadas por una revisión.

Si una revisión agrega o actualiza una acción personalizada con el atributo **msidbCustomActionTypePatchUninstall** , Windows Installer ejecutará la acción personalizada nueva o actualizada cuando se desinstale la revisión. Windows Installer hace que las actualizaciones de la revisión se desinstalen disponibles para la acción personalizada desinstalar revisión. La revisión debe incluir una *<PatchGUID>* tabla MsiTransformView para proporcionar esta información a Windows Installer. La información de esta tabla está disponible para cualquier acción personalizada inmediata y no está disponible para las acciones personalizadas diferidas.

**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible. La [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) está disponible a partir de Windows Installer 4,5.

Esta tabla se debe denominar MsiTransformView *<PatchGUID>* TABLE, donde *<PatchGUID>* es el GUID que identifica la revisión de forma única. La *<PatchGUID>* tabla MsiTransformView tiene las columnas siguientes.



| Columna  | Tipo                         | Clave | Nullable |
|---------|------------------------------|-----|----------|
| Tabla   | [Identificador](identifier.md) | Y   | N        |
| Columna  | [Texto](text.md)             | Y   | N        |
| Row     | [Texto](text.md)             | Y   | Y        |
| Datos    | [Texto](text.md)             | N   | Y        |
| Current | [Texto](text.md)             | N   | Y        |



 

## <a name="column"></a>Columna

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro
</dt> <dd>

Nombre de una tabla de base de datos modificada.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Artículo
</dt> <dd>

Nombre de una columna de tabla alterada o inserción, eliminación, creación o eliminación.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Columna
</dt> <dd>

Una lista de los valores de clave principal separados por tabulaciones. Los valores de clave principal NULL se representan mediante un solo carácter de espacio. Un valor null en esta columna indica un cambio de esquema.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Data
</dt> <dd>

Los datos, el nombre de un flujo de datos o una definición de columna.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Corrientes
</dt> <dd>

Valor actual de la base de datos de referencia o de una columna a un número.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Revisión desinstalar las acciones personalizadas se ejecutan cuando se desinstala la revisión. No se ejecutan cuando se desinstala el producto. Use la [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) y esta tabla para ejecutar una personalizada solo cuando se desinstale la revisión.

Una revisión puede actualizar una acción personalizada proporcionada en el paquete original (archivo. msi). Para ejecutar la versión actualizada de la acción personalizada cuando se desinstale la revisión, marque la acción personalizada con el atributo **msidbCustomActionTypePatchUninstall** en el paquete original.

 

 



