---
description: Cada Active Directory objeto tiene un descriptor de seguridad asignado.
ms.assetid: 2e4ed13f-f09e-43b4-9862-95a79c229f0c
title: Derechos de acceso de servicios de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f24e75db6733a8f5833e7f45ab5a52dafd67f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278999"
---
# <a name="directory-services-access-rights"></a>Derechos de acceso de servicios de directorio

Cada Active Directory objeto tiene un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) asignado. Se puede establecer un conjunto de derechos de confianza específicos de los objetos de servicio de directorio dentro de estos descriptores de seguridad. Estos derechos se muestran en la tabla siguiente. Para obtener más información, vea [controlar derechos de acceso](/windows/desktop/AD/control-access-rights).



| Derechos                                | Significado                                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTRL \_ DS \_ abierto<br/>            | Abra un objeto DS.<br/>                                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ crear \_ secundario<br/>   | Cree un objeto DS secundario.<br/>                                                                                                                                                                                                                                                    |
| ACTRL \_ DS \_ eliminar \_ secundario<br/>   | Elimine un objeto DS secundario.<br/>                                                                                                                                                                                                                                                    |
| lista de ACTRL \_ DS \_<br/>            | Enumerar un objeto DS.<br/>                                                                                                                                                                                                                                                       |
| ACTRL \_ DS \_ lectura \_ prop<br/>      | Leer las propiedades de un objeto DS.<br/>                                                                                                                                                                                                                                          |
| PROP de escritura de ACTRL \_ DS \_ \_<br/>     | Escribir propiedades para un objeto DS.<br/>                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ Self<br/>            | Acceso permitido solo después de que se realicen las comprobaciones de derechos validadas admitidas por el objeto. Esta marca se puede usar solo para realizar todas las comprobaciones de derechos validadas del objeto o se puede combinar con un identificador de un derecho específico validado para realizar solo esa comprobación.<br/> |
| ACTRL \_ \_ árbol de eliminación de DS \_<br/>    | Elimina un árbol de objetos de DS.<br/>                                                                                                                                                                                                                                                 |
| ACTRL \_ \_ objeto de lista de DS \_<br/>    | Muestra un árbol de objetos de DS.<br/>                                                                                                                                                                                                                                                   |
| ACTRL \_ \_ acceso de control de DS \_<br/> | Acceso permitido solo después de que se realicen las comprobaciones de derechos extendidas admitidas por el objeto. Esta marca se puede usar solo para realizar todas las comprobaciones de derechos extendidos en el objeto o puede combinarse con un identificador de un derecho extendido específico para realizar solo esa comprobación.<br/>    |



 

 

