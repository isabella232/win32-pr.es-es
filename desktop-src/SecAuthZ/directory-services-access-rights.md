---
description: Cada Active Directory objeto tiene asignado un descriptor de seguridad.
ms.assetid: 2e4ed13f-f09e-43b4-9862-95a79c229f0c
title: Derechos de acceso de servicios de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901c8eba5736750e0c91eb713993876c47858407110ca3c8ebc6ed8122e1b8d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913768"
---
# <a name="directory-services-access-rights"></a>Derechos de acceso de servicios de directorio

Cada Active Directory objeto tiene asignado un [*descriptor*](/windows/desktop/SecGloss/s-gly) de seguridad. Se puede establecer un conjunto de derechos de administrador específicos de los objetos de servicio de directorio dentro de estos descriptores de seguridad. Estos derechos se enumeran en la tabla siguiente. Para obtener más información, vea [Controlar los derechos de acceso.](/windows/desktop/AD/control-access-rights)



| Derechos                                | Significado                                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTRL \_ DS \_ OPEN<br/>            | Abra un objeto DS.<br/>                                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ CREATE \_ CHILD<br/>   | Cree un objeto DS secundario.<br/>                                                                                                                                                                                                                                                    |
| ACTRL \_ DS \_ DELETE \_ CHILD<br/>   | Elimina un objeto DS secundario.<br/>                                                                                                                                                                                                                                                    |
| ACTRL \_ DS \_ LIST<br/>            | Enumerar un objeto DS.<br/>                                                                                                                                                                                                                                                       |
| ACTRL \_ DS \_ READ \_ PROP<br/>      | Lea las propiedades de un objeto DS.<br/>                                                                                                                                                                                                                                          |
| ACTRL \_ DS \_ WRITE \_ PROP<br/>     | Escribir propiedades para un objeto DS.<br/>                                                                                                                                                                                                                                            |
| ACTRL \_ DS \_ SELF<br/>            | Acceso permitido solo después de que se realicen comprobaciones de derechos validadas admitidas por el objeto. Esta marca se puede usar por sí sola para realizar todas las comprobaciones de derechos validados del objeto o se puede combinar con un identificador de un derecho validado específico para realizar solo esa comprobación.<br/> |
| ÁRBOL DE ELIMINACIÓN DE ACTRL \_ DS \_ \_<br/>    | Elimine un árbol de objetos DS.<br/>                                                                                                                                                                                                                                                 |
| ACTRL \_ DS \_ LIST \_ (OBJETO)<br/>    | Enumera un árbol de objetos DS.<br/>                                                                                                                                                                                                                                                   |
| ACTRL \_ DS \_ CONTROL \_ ACCESS<br/> | Acceso permitido solo después de realizar comprobaciones de derechos extendidos admitidas por el objeto. Esta marca se puede usar por sí sola para realizar todas las comprobaciones de derechos extendidos en el objeto o se puede combinar con un identificador de un derecho extendido específico para realizar solo esa comprobación.<br/>    |



 

 

