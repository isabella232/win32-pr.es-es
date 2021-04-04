---
title: Atributos de encabezado de interfaz
description: Incorpore estos atributos en el encabezado de la interfaz para transmitir información sobre toda la interfaz.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- MIDL, atributos y encabezado de interfaz IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075528"
---
# <a name="interface-header-attributes"></a>Atributos de encabezado de interfaz

Incorpore estos atributos en el encabezado de la interfaz para transmitir información sobre toda la interfaz.



| Atributo                                   | Uso                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_UUID asincrónico**](async-uuid.md)           | Indica al compilador de MIDL que defina las versiones sincrónicas y asincrónicas de una interfaz COM.                                                                                                                                               |
| [**uuid**](uuid.md)                        | Designa un valor de 128 bits que distingue una interfaz determinada de las demás. El valor real puede representar un GUID, un CLSID o un IID.                                                                                                 |
| [**localizar**](local.md)                      | Indica al compilador de MIDL que genere solo archivos de encabezado. Una interfaz debe tener un [**UUID**](uuid.md) o un atributo [**local**](local.md) .                                                                                             |
| [**Unión de MS \_**](-ms-union.md)              | Controla la alineación del NDR de las uniones no encapsuladas. Se utiliza para la compatibilidad con versiones anteriores con interfaces basadas en MIDL 1,0 o 2,0.                                                                                                                   |
| [**objeto**](object.md)                    | Identifica la interfaz como una interfaz COM y dirige el compilador de MIDL para que genere código de proxy o código auxiliar en lugar de los códigos auxiliares de cliente y servidor de RPC.                                                                                                    |
| [**Versión**](version.md)                  | Identifica una versión concreta de una interfaz en los casos en que existen varias versiones de la interfaz. Dado que las interfaces COM son inmutables, no puede usar el atributo [**version**](version.md) en una interfaz de [**objeto**](object.md) . |
| [**puntero \_ predeterminado**](pointer-default.md) | Especifica el tipo de puntero predeterminado para todos los punteros excepto los incluidos en las listas de parámetros. El tipo predeterminado puede ser [**Unique**](unique.md), [**ref**](ref.md)o [**ptr**](ptr.md).                                                   |
| [**finales**](endpoint.md)                | Especifica un punto de conexión estático (conocido) en el que una aplicación de servidor escuchará las llamadas a procedimientos remotos.                                                                                                                                   |



 

Vea [atributos](type-library-attributes.md) de la biblioteca de tipos para los atributos de interfaz, como [**dual**](dual.md) y [**oleautomation**](oleautomation.md), que son específicos de las interfaces definidas o a las que se hace referencia dentro de una instrucción Library.

 

 




