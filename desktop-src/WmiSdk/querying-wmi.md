---
description: Una de las principales herramientas de Instrumental de administración de Windows (WMI) es la capacidad de consultar el repositorio WMI para obtener información sobre la clase y la instancia.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Consultando WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdae44d4c40e1127bfc4d3436d6230eafd52146a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696804"
---
# <a name="querying-wmi"></a>Consultando WMI

Una de las principales herramientas de Instrumental de administración de Windows (WMI) es la capacidad de consultar el repositorio WMI para obtener información sobre la clase y la instancia. Por ejemplo, puede solicitar que WMI devuelva todos los objetos que representan los eventos de cierre del sistema de escritorio. También puede recuperar los datos de la clase, la instancia o el esquema. En la tabla siguiente se enumeran los diferentes tipos de consultas que se pueden realizar.



| Tema                                                                | Descripción                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Invocar una consulta sincrónica](invoking-a-synchronous-query.md)     | Describe cómo mantener un vínculo con WMI a lo largo del proceso de consulta. Las consultas sincrónicas son adecuadas para consultas pequeñas o consultas en un sistema local.<br/>                                  |
| [Invocar una consulta asincrónica](invoking-an-asynchronous-query.md) | Describe cómo configurar un proceso independiente para recibir consultas. Las consultas asincrónicas son más complejas y proporcionan un nivel inferior de seguridad, pero, por lo general, mejoran el rendimiento del sistema.<br/> |



 

Además de consultar el repositorio WMI, también puede usar el [*lenguaje de consulta de WMI (WQL)*](gloss-w.md) para enrutar los eventos de notificación a la aplicación. Para obtener más información, consulte [recibir un evento WMI](receiving-a-wmi-event.md).

> [!Note]
>
> Para consultar correctamente WMI, debe tener una buena comprensión de WQL. Una consulta incorrecta, demasiado compleja o inapropiada puede hacer que el procesador de consultas devuelva un error o resultados inesperados. Para obtener una guía completa de WQL, vea [consultas con WQL](querying-with-wql.md).
>
> Hay límites en el número de palabras clave **and** y **or** que se pueden usar en las consultas WQL. Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el código de error de **\_ \_ \_ infracción de la cuota de WBEM E** como un valor **HRESULT** . El límite de palabras clave de WQL depende de la complejidad de la consulta.
>
> Al consultar los valores de propiedad con un tipo de datos **UInt64** o **sint64** en un lenguaje de scripting como VBScript, WMI devuelve valores de cadena. Pueden producirse resultados inesperados al comparar estos valores, ya que la comparación de cadenas devuelve resultados diferentes a los de la comparación de números. Por ejemplo, "10 mil millones" es menor que "9" al comparar cadenas y 9 es inferior a 10 mil millones al comparar números. Para evitar confusiones, debe utilizar el método [CDbl](/previous-versions//ftekwwt0(v=vs.85)) en VBScript cuando las propiedades de tipo **UInt64** o **SINT64** se recuperan de WMI.

 

> [!Note]  

 

Para obtener más información, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md).

 

