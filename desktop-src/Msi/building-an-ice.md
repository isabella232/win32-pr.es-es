---
description: Si no puede encontrar los evaluadores de coherencia internos que necesita entre las acciones personalizadas de ICE existentes enumeradas en la referencia de ICE, tendrá que preparar su propia ICE para validar el paquete.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Creación de un ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667010"
---
# <a name="building-an-ice"></a>Creación de un ICE

Si no puede encontrar los [evaluadores de coherencia internos](internal-consistency-evaluators-ices.md) que necesita entre las acciones personalizadas de ICE existentes enumeradas en la [referencia de ICE](ice-reference.md), tendrá que preparar su propia ICE para validar el paquete.

Al crear acciones personalizadas de ICE, debe hacer lo siguiente:

-   Basar el ICEs solo en acciones personalizadas de los tipos que aparecen en la tabla mostrada.
-   Llame a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) y publique un \_ tipo de usuario de INSTALLMESSAGE de mensaje. Al crear los mensajes ICE, siga el formato del mensaje en las [instrucciones del mensaje de ICE](ice-message-guidelines.md).
-   Escriba el ICE de modo que capture cualquier error de API y siempre devuelva el ERROR \_ correcto. Esto es necesario para permitir que se ejecuten las acciones personalizadas posteriores después del error de un ICE.

Las acciones personalizadas de ICE se limitan a los siguientes tipos de acciones personalizadas.



| Tipo de acción personalizada                                 | Descripción               |
|----------------------------------------------------|---------------------------|
| [Tipo de acción personalizada 1](custom-action-type-1.md)   | DLL en secuencia binaria      |
| [Tipo de acción personalizada 2](custom-action-type-2.md)   | EXE en una secuencia binaria      |
| [Tipo de acción personalizada 5](custom-action-type-5.md)   | JScript en secuencia binaria  |
| [Tipo de acción personalizada 6](custom-action-type-6.md)   | VBScript en una secuencia binaria |
| [Tipo de acción personalizada 37](custom-action-type-37.md) | Código JScript como cadena    |
| [Tipo de acción personalizada 38](custom-action-type-38.md) | Código VBScript como cadena   |



 

Al crear una acción personalizada ICE, no haga lo siguiente:

-   No asuma que el identificador del motor que recibe el ICE es una instancia de instalación de la base de datos del instalador. Si no es una instancia de instalación, no se han definido determinadas propiedades, no se resuelven los directorios de origen y de destino, y no se definen los Estados de las características actuales.
-   No confíe en la ejecución anterior, o no en la ejecución, de cualquier acción del instalador, acción personalizada u otro ICE. Dado que una ICE anterior puede haber creado columnas temporales en una tabla, los autores deben hacer referencia a las columnas por nombre siempre que sea posible. ICEs debe limpiar las columnas o tablas temporales antes de salir.
-   No asuma que los autores tienen acceso a una imagen del directorio de origen de la base de datos.
-   No asuma que los cambios realizados en la base de datos no se conservan.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ICE de ejemplo en C++](sample-ice-in-c-.md)
</dt> <dt>

[ICE de ejemplo en VBScript](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



