---
description: Los siguientes códigos de error son específicos de la API de instalación.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Códigos de error (API de instalación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497903"
---
# <a name="error-codes-setup-api"></a>Códigos de error (API de instalación)

Los siguientes códigos de error son específicos de la API de instalación.



| Errores de análisis de INF              | Descripción                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| ERROR \_ en \_ el nombre de sección esperado \_  | Se esperaba un nombre de sección y no se encontró.                                                                          |
| ERROR \_ \_ en la \_ línea de nombre de sección incorrecta \_ | El nombre de la sección no tenía el formato correcto. (Por ejemplo, un nombre que no termina con un corchete de cierre ( \] ). |
| nombre de sección de ERROR \_ \_ \_ demasiado \_ largo | El nombre de sección superó la longitud máxima del nombre máximo de la sección longitud \_ \_ \_ .                                               |
| ERROR \_ General de \_ Sintaxis          | La sintaxis general es incorrecta.                                                                                    |



 



| Errores en tiempo de ejecución de INF         | Descripción                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR \_ de \_ estilo INF incorrecto \_   | El archivo INF no es del tipo especificado en la llamada de función. Por ejemplo, este error puede ser devuelto por la función [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) si el archivo INF estaba destinado a una versión anterior de Windows. |
| \_ \_ no \_ se encontró la sección de error | No se encontró la sección en el archivo INF.                                                                                                                                                                                                     |
| \_ \_ no \_ se encontró la línea de error    | No se encontró la línea en la sección INF.                                                                                                                                                                                                     |



 

 

 



