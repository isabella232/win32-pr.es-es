---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: f1b94241-5376-423f-b10a-336dc47f3d59
title: Nota para autores de GPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942bd1e8725428ee49bb937f3978622413160476
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689690"
---
# <a name="note-to-gpd-authors"></a>Nota para autores de GPD

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En el caso de los autores de documentos de PrintCapabilities que están familiarizados con los archivos GPD, algunas palabras clave de GPD no tienen equivalentes en el documento de PrintCapabilities. La tabla siguiente contiene las palabras clave de GPD sin un documento de PrintCapabilities equivalente y la razón por la que no hay ningún equivalente.



| Palabra clave GPD                                                                            | Explicación                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*Restricciones<br/> \*InvalidCombination<br/> \*ConflictPriority<br/> | Las restricciones no se definen en el documento de PrintCapabilities porque no se espera que los clientes de PrintCapabilities los procesen, apliquen o resuelvan. Estas tareas se dejan para que el proveedor de PrintTicket realice durante la validación de PrintTicket. Los complementos unidrv pueden proporcionar su propio código de validación de PrintTicket, o bien se pueden basar en unidrv para llevar a cabo esta validación. En el último caso, unidrv aplica todas las restricciones definidas en el archivo GPD.<br/> Los controladores monolíticos deben proporcionar su propio código de validación de PrintTicket y deben proporcionar su propio método para expresar y aplicar restricciones.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \*DefaultOption<br/>                                                             | Hay un método PrintTicket que devuelve un PrintTicket predeterminado, que por definición tiene todos los valores predeterminados para cada característica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \*FeatureType<br/>                                                               | Una característica se puede dividir en tres categorías diferentes:<br/> Característica cuya configuración se define en un PrintTicket. Este tipo de característica se denomina "adhesiva de documento", ya que esta configuración determina directamente la manera en la que se procesa un documento.<br/> Característica cuya configuración refleja atributos de dispositivo físico que no son controlados por el usuario, como la cantidad de memoria del dispositivo o que indican la presencia de complementos opcionales como alimentadores de papel o dúplex. Este tipo de característica se denomina dispositivo o impresora adhesiva. El estado de este tipo de característica es importante, ya que puede restringir una opción que pertenezca a una característica adhesiva de documentos.<br/> Una característica adhesiva de dispositivo o impresora se puede clasificar aún más como una característica adhesiva de impresora de la interfaz de usuario o como una característica de impresora adhesiva automática. Una característica de impresión permanente de la interfaz de usuario se debe mostrar en una interfaz de usuario que un administrador puede establecer. El dispositivo detecta automáticamente una característica de impresora adhesiva automática.<br/> |
| \*Cambiar. \* .. Y<br/>                                                         | Un proveedor de PrintCapabilities debe implementar un método que crea un documento de PrintCapabilities que enumera las características adhesivas de impresión o de documentos, dependiendo del tipo especificado por el autor de la llamada. Por esta razón, no es necesario presentar la misma información a través del propio documento de PrintCapabilities.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




