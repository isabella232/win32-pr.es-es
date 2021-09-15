---
description: Hay algunas consideraciones que son únicas para los sistemas administrados de forma remota.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Consideraciones sobre la administración remota de WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359858"
---
# <a name="wfp-remote-administration-considerations"></a>Consideraciones sobre la administración remota de WFP

Hay algunas consideraciones que son únicas para los sistemas administrados de forma remota. En primer lugar, cuando la instalación de software se implementa de forma remota (mediante SMS o MSI), los cuadros de diálogo de error de WFP se muestran en la pantalla de un administrador que ha iniciado sesión localmente (si está presente), no en el servicio de instalación. En segundo lugar, si un administrador inicia sesión en un servidor de terminal de forma remota e instala una aplicación que reemplaza los archivos del sistema protegidos, los cuadros de diálogo de error de WFP solo se muestran en la consola principal, no en la ventana remota del administrador.

Por estos motivos, WFP suprime sus cuadros de diálogo de error hasta que un administrador inicia sesión localmente. Los administradores remotos pueden encontrar errores de reemplazo de archivos en el registro de eventos del sistema.

**Windows Vista y Windows Server 2008:** No se admite la administración remota de WFP.

 

 



