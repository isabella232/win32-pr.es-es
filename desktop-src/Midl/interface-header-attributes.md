---
title: Atributos de encabezado de interfaz
description: Incorpore estos atributos en el encabezado de interfaz para transmitir información sobre toda la interfaz.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL MIDL, atributos, encabezado de interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159523"
---
# <a name="interface-header-attributes"></a>Atributos de encabezado de interfaz

Incorpore estos atributos en el encabezado de interfaz para transmitir información sobre toda la interfaz.



| Atributo                                   | Uso                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**uuid \_ asincrónico**](async-uuid.md)           | Dirige al compilador MIDL para definir las versiones sincrónicas y asincrónicas de una interfaz COM.                                                                                                                                               |
| [**Uuid**](uuid.md)                        | Designa un valor de 128 bits que distingue una interfaz determinada de todas las demás. El valor real puede representar un GUID, un CLSID o un IID.                                                                                                 |
| [**Local**](local.md)                      | Dirige al compilador MIDL para que genere solo archivos de encabezado. Una interfaz debe tener un [**uuid**](uuid.md) o un [**atributo local.**](local.md)                                                                                             |
| [**ms \_ union**](-ms-union.md)              | Controla la alineación BAND de las uniones nocapsuladas. Se usa para la compatibilidad con versiones anteriores con interfaces creadas en MIDL 1.0 o 2.0.                                                                                                                   |
| [**object**](object.md)                    | Identifica la interfaz como una interfaz COM y dirige al compilador MIDL para que genere código proxy/stub en lugar de código auxiliar de cliente y servidor RPC.                                                                                                    |
| [**version**](version.md)                  | Identifica una versión determinada de una interfaz en los casos en los que existen varias versiones de la interfaz. Dado que las interfaces COM son inmutables, no se puede usar el [**atributo version**](version.md) en una [**interfaz de**](object.md) objeto. |
| [**valor \_ predeterminado del puntero**](pointer-default.md) | Especifica el tipo de puntero predeterminado para todos los punteros, excepto los incluidos en las listas de parámetros. El tipo predeterminado puede ser [**único,**](unique.md) [**ref**](ref.md)o [**ptr.**](ptr.md)                                                   |
| [**endpoint**](endpoint.md)                | Especifica un punto de conexión estático (conocido) en el que una aplicación de servidor escuchará las llamadas a procedimiento remoto.                                                                                                                                   |



 

Vea [Atributos de la biblioteca de](type-library-attributes.md) tipos para los atributos de interfaz, como [**dual**](dual.md) y [**oleautomation,**](oleautomation.md)que son específicos de las interfaces definidas o a las que se hace referencia dentro de una instrucción de biblioteca.

 

 




