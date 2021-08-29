---
description: Revise las palabras clave GPD sin equivalentes de documento PrintCapabilities. Este tema no está al día. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: f1b94241-5376-423f-b10a-336dc47f3d59
title: Nota para los autores de GPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce16d78d5b9ed088b0d33616eca781dec9e83c89e94e35477f34e7e96579ba84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098969"
---
# <a name="note-to-gpd-authors"></a>Nota para los autores de GPD

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Para los autores de documentos de PrintCapabilities que están familiarizados con los archivos GPD, algunas palabras clave GPD no tienen equivalentes en el documento PrintCapabilities. La tabla siguiente contiene las palabras clave GPD sin un documento PrintCapabilities equivalente y el motivo no es equivalente.



| Palabra clave GPD                                                                            | Explicación                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*Restricciones<br/> \*InvalidCombination<br/> \*ConflictPriority<br/> | Las restricciones no se definen en el documento PrintCapabilities porque no se espera que los clientes de PrintCapabilities las procesen, exijan ni resuelvan. Estas tareas se quedan para que el proveedor PrintTicket realice durante la validación de PrintTicket. Los complementos Unidrv pueden proporcionar su propio código de validación PrintTicket, o bien pueden confiar en Unidrv para llevar a cabo esta validación. En el último caso, Unidrv aplica las restricciones definidas en el archivo GPD.<br/> Los controladores monolíticos deben proporcionar su propio código de validación PrintTicket y deben proporcionar su propio método para expresar y aplicar restricciones.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \*DefaultOption<br/>                                                             | Hay un método PrintTicket que devuelve un PrintTicket predeterminado, que por definición tiene toda la configuración predeterminada para cada característica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \*FeatureType<br/>                                                               | Una característica se puede dividir en tres categorías diferentes:<br/> Característica cuya configuración se define en printticket. Este tipo de característica se denomina permanente al documento porque esta configuración determina directamente la manera en que se procesa un documento.<br/> Característica cuya configuración refleja atributos de dispositivo físico que no están controlados por el usuario, como la cantidad de memoria del dispositivo, o que indican la presencia de complementos opcionales, como fuentes de papel o dúplex. Este tipo de característica se denomina dispositivo permanente o permanente para la impresora. El estado de este tipo de característica es importante porque puede restringir una opción que pertenece a una característica permanente del documento.<br/> Una característica permanente del dispositivo o la característica permanente de la impresora se puede clasificar aún más como una característica permanente de la impresora de la interfaz de usuario (UI) o una característica permanente de la impresora automática. Una característica permanente de la impresora de la interfaz de usuario debe mostrarse en una interfaz de usuario que un administrador pueda establecer. El dispositivo detecta automáticamente una característica permanente de la impresora automática.<br/> |
| \*Cambiar ... \* Caso<br/>                                                         | Un proveedor printCapabilities debe implementar un método que cree un documento PrintCapabilities que enumere las características permanentes de la impresora o las características permanentes del documento, en función del tipo especificado por el autor de la llamada. Por este motivo, no es necesario presentar la misma información a través del propio documento PrintCapabilities.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




