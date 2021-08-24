---
description: El modo de error indica al sistema cómo responderá la aplicación a errores graves.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Modo de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a1baa4c0bc4e1209586b630f2a58bfb06572131de8e7d2706614c78646d7e3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260935"
---
# <a name="error-mode"></a>Modo de error

El modo de error indica al sistema cómo responderá la aplicación a errores graves. Los errores graves incluyen errores de disco, errores de unidad no preparada, desalineación de datos y excepciones no controladas. Este modo de error se puede administrar por subproceso o por proceso. Una aplicación puede permitir que el sistema muestre un cuadro de mensaje que informa al usuario de que se ha producido un error o puede controlar los errores.

Para controlar estos errores sin intervención del usuario, use [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) o [**setThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)específico del subproceso. Después de llamar a una de estas funciones y especificar las marcas adecuadas, el sistema no mostrará los cuadros de mensaje de error correspondientes.

Un proceso puede recuperar su modo de error [**mediante GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) o [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).

El procedimiento recomendado es que todas las aplicaciones llamen a la función [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) de todo el proceso con un parámetro **de SEM \_ FAILCRITICALERRORS en** el inicio. Esto es para evitar que los cuadros de diálogo de modo de error se queme la aplicación.

Aparte de eso, los llamadores deben favorecer las versiones específicas del subproceso de estas funciones, ya que son menos perjudiciales para el comportamiento normal del sistema.

 

 
