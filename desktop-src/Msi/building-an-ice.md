---
description: Si no encuentra los evaluadores de coherencia internos que necesita entre las acciones personalizadas de ICE existentes enumeradas en la referencia de ICE, deberá preparar su propio ICE para validar el paquete.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Creación de un ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4b79ab8e17d53ccfb60484c0d307f668c44a7a0e530cf776b10e73a697541c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500774"
---
# <a name="building-an-ice"></a>Creación de un ICE

Si no encuentra los evaluadores de coherencia interna que necesita entre las acciones personalizadas de ICE [existentes](internal-consistency-evaluators-ices.md) enumeradas en la referencia de [ICE,](ice-reference.md)deberá preparar su propio ICE para validar el paquete.

Al crear acciones personalizadas de ICE, debe hacer lo siguiente:

-   Base los TIC solo en acciones personalizadas de los tipos enumerados en la tabla que se muestra.
-   Llame [**a MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) y publique un tipo de mensaje INSTALLMESSAGE \_ USER. Al crear los mensajes de ICE, siga el formato del mensaje en las instrucciones [de mensaje de ICE](ice-message-guidelines.md).
-   Escriba el ICE de modo que capture los errores de API y siempre devuelva ERROR \_ SUCCESS. Esto es necesario para permitir que las acciones personalizadas posteriores se ejecuten después del error de un ICE.

Las acciones personalizadas de ICE se limitan a los siguientes tipos de acciones personalizadas.



| Tipo de acción personalizada                                 | Descripción               |
|----------------------------------------------------|---------------------------|
| [Tipo de acción personalizada 1](custom-action-type-1.md)   | DLL en secuencia binaria      |
| [Tipo de acción personalizada 2](custom-action-type-2.md)   | EXE en secuencia binaria      |
| [Tipo de acción personalizada 5](custom-action-type-5.md)   | JScript en secuencia binaria  |
| [Tipo de acción personalizada 6](custom-action-type-6.md)   | VBScript en secuencia binaria |
| [Tipo de acción personalizada 37](custom-action-type-37.md) | JScript código como cadena    |
| [Tipo de acción personalizada 38](custom-action-type-38.md) | Código VBScript como cadena   |



 

Al crear una acción personalizada de ICE, no haga lo siguiente:

-   No suponga que el identificador del motor que recibe el ICE es una instancia de instalación de la base de datos del instalador. Si no es una instancia de instalación, no se definen determinadas propiedades, los directorios de origen y destino no se resuelven y no se definen los estados de características actuales.
-   No se base en la ejecución anterior o no ejecutada de ninguna acción del instalador, acción personalizada u otro ICE. Dado que un ICE anterior puede haber creado columnas temporales en cualquier tabla, los autores deben hacer referencia a las columnas por nombre siempre que sea posible. Los TIC deben limpiar las columnas o tablas temporales antes de salir.
-   No suponga que los autores tienen acceso a una imagen del directorio de origen de la base de datos.
-   No suponga que los cambios realizados en la base de datos no se conservan.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ICE de ejemplo en C++](sample-ice-in-c-.md)
</dt> <dt>

[ICE de ejemplo en VBScript](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



