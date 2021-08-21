---
description: Una de las herramientas principales de Windows Management Instrumentation (WMI) es la capacidad de consultar la información de clase e instancia en el repositorio WMI.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Consulta de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc9cd51946bad1df482bb286c538e38bba8e2b3337776e3cd62e0a0da652574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817543"
---
# <a name="querying-wmi"></a>Consulta de WMI

Una de las herramientas principales de Windows Management Instrumentation (WMI) es la capacidad de consultar la información de clase e instancia en el repositorio WMI. Por ejemplo, puede solicitar que WMI devuelva todos los objetos que representan eventos de apagado desde el sistema de escritorio. También puede recuperar datos de clase, instancia o esquema. En la tabla siguiente se enumeran los distintos tipos de consultas que puede realizar.



| Tema                                                                | Descripción                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Invocación de una consulta sincrónica](invoking-a-synchronous-query.md)     | Describe cómo mantener un vínculo con WMI a lo largo del proceso de consulta. Las consultas sincrónicas son buenas para consultas pequeñas o consultas en un sistema local.<br/>                                  |
| [Invocación de una consulta asincrónica](invoking-an-asynchronous-query.md) | Describe cómo configurar un proceso independiente para recibir consultas. Las consultas asincrónicas son más complejas y proporcionan un nivel de seguridad inferior, pero generalmente mejoran el rendimiento del sistema.<br/> |



 

Además de consultar el repositorio WMI, también puede usar el lenguaje de consulta de WMI [*(WQL)*](gloss-w.md) para enrutar eventos de notificación a la aplicación. Para obtener más información, vea [Recibir un evento WMI](receiving-a-wmi-event.md).

> [!Note]
>
> Para consultar correctamente WMI, debe tener una buena comprensión de WQL. Una consulta incorrecta, demasiado compleja o inapropiada puede hacer que el procesador de consultas devuelva un error o resultados inesperados. Para obtener una guía completa de WQL, consulte [Consulta con WQL.](querying-with-wql.md)
>
> Hay límites en el número de palabras clave **AND** **y OR** que se pueden usar en consultas WQL. Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el código de error **WBEM \_ E QUOTA \_ \_ VIOLATION** como **un valor HRESULT.** El límite de palabras clave WQL depende de lo compleja que sea la consulta.
>
> Al consultar valores de propiedad con un tipo de datos **uint64** o **sint64** en un lenguaje de scripting como VBScript, WMI devuelve valores de cadena. Se pueden producir resultados inesperados al comparar estos valores, ya que la comparación de cadenas devuelve resultados diferentes a los de la comparación de números. Por ejemplo, "100000000000" es menor que "9" al comparar cadenas y 9 es menor que 10000000000 al comparar números. Para evitar confusiones, debe usar el [método CDbl](/previous-versions//ftekwwt0(v=vs.85)) en VBScript cuando las propiedades de tipo **uint64** o **sint64** se recuperan de WMI.

 

> [!Note]  

 

Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

 

