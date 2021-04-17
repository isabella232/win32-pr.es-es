---
description: La tabla CCPSearch contiene la lista de firmas de archivo que se usan para el programa de comprobación de cumplimiento (CCP). Al menos uno de estos archivos debe estar presente en el equipo de un usuario para que el usuario cumpla con el programa.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Tabla CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667005"
---
# <a name="ccpsearch-table"></a>Tabla CCPSearch

La tabla CCPSearch contiene la lista de firmas de archivo que se usan para el programa de comprobación de cumplimiento (CCP). Al menos uno de estos archivos debe estar presente en el equipo de un usuario para que el usuario cumpla con el programa.

La tabla CCPSearch tiene la siguiente columna.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Signatura\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="column"></a>Columna

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_
</dt> <dd>

La firma \_ representa una firma de archivo única y también es la clave externa en las tablas [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)y [DrLocator](drlocator-table.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta la acción [CCPSearch](ccpsearch-action.md) o la [acción RMCCPSearch](rmccpsearch-action.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



