---
title: Atributos ACF de control de errores y excepciones
description: Utilice los siguientes atributos para el control de errores.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- Los MIDL, atributos, errores y control de excepciones de ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685708"
---
# <a name="error-and-exception-handling-acf-attributes"></a>Atributos ACF de control de errores y excepciones

Utilice los siguientes atributos para el control de errores.



| Atributo                                                                | Uso                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Estado de error de [**\_ Estado de comunicación**](comm-status.md)[**\_**](fault-status.md) | Permita que la aplicación cliente controle las excepciones correctamente provocando que los errores del servidor y la comunicación se devuelvan al cliente como valores de parámetro. A continuación, la aplicación cliente puede llamar a la función de tiempo de ejecución de RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) para retransmitir un mensaje de error al usuario. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Importar archivos y bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> </dl>

 

 