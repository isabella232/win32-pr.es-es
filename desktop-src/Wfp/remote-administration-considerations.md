---
description: Hay algunas consideraciones que son exclusivas de los sistemas administrados de forma remota.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Consideraciones sobre la administración remota de WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706853"
---
# <a name="wfp-remote-administration-considerations"></a>Consideraciones sobre la administración remota de WFP

Hay algunas consideraciones que son exclusivas de los sistemas administrados de forma remota. En primer lugar, cuando la instalación de software se implementa de forma remota (mediante SMS o MSI), los cuadros de diálogo de error de WFP se muestran en la pantalla de un administrador con sesión iniciada localmente (si existe), no en el servicio de instalación. En segundo lugar, si un administrador inicia sesión en un servidor de Terminal Server de forma remota e instala una aplicación que reemplaza los archivos del sistema protegidos, los cuadros de diálogo de error de WFP solo se muestran en la consola principal, no en la ventana remota del administrador.

Por estos motivos, WFP suprime los cuadros de diálogo de error hasta que un administrador inicia sesión localmente. Los administradores remotos pueden encontrar errores de reemplazo de archivos en el registro de eventos del sistema.

**Windows Vista y Windows Server 2008:** No se admite la administración remota de WFP.

 

 



