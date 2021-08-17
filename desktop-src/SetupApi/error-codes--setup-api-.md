---
description: Los siguientes códigos de error son específicos de la API de instalación.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Códigos de error (API de instalación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c3955bd64f38946a59589259fc750892cfa9e84b3ef6e32ba2d9a5f6ca2244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887344"
---
# <a name="error-codes-setup-api"></a>Códigos de error (API de instalación)

Los siguientes códigos de error son específicos de la API de instalación.



| Errores de análisis de INF              | Descripción                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| ERROR \_ SE ESPERABA NOMBRE DE \_ \_ SECCIÓN  | Se esperaba un nombre de sección y no se encontró.                                                                          |
| ERROR \_ BAD \_ SECTION \_ NAME \_ LINE | El nombre de la sección no tenía el formato correcto. (Por ejemplo, un nombre no terminado por un corchete de la derecha ( \] ). |
| ERROR \_ SECTION \_ NAME \_ TOO \_ LONG | El nombre de la sección superó la longitud máxima de MAX \_ SECT \_ NAME \_ LEN.                                               |
| ERROR \_ SINTAXIS GENERAL \_          | La sintaxis general es incorrecta.                                                                                    |



 



| Errores en tiempo de ejecución de INF         | Descripción                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR \_ DE ESTILO INF \_ \_ INCORRECTO   | El archivo INF no es del tipo especificado en la llamada de función. Por ejemplo, la función [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) puede devolver este error si el archivo INF estaba pensado para una versión anterior de Windows. |
| NO \_ SE ENCONTRÓ LA SECCIÓN \_ \_ ERROR | La sección no se encontró en el archivo INF.                                                                                                                                                                                                     |
| NO SE \_ ENCONTRÓ LA LÍNEA DE \_ \_ ERROR    | La línea no se encontró en la sección INF.                                                                                                                                                                                                     |



 

 

 



