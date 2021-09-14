---
title: Ámbito de la consulta
description: El ámbito de una consulta viene determinado por el objeto al que se enlaza.
ms.assetid: 7ece8599-8a4b-45a1-95f4-a4180052f245
ms.tgt_platform: multiple
keywords:
- ámbito de ADSI de consulta
- consulta ADSI, ámbito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac51fc261cb418db0018acd996c248766896a25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172173"
---
# <a name="scope-of-query"></a>Ámbito de la consulta

El ámbito de una consulta viene determinado por el objeto al que se enlaza. Si no está seguro de dónde se encuentra el objeto dentro de la empresa, deberá realizar una búsqueda lo más amplia posible. Sin embargo, si sabe que el objeto se incluirá dentro de un dominio específico, como el dominio al que está conectado el usuario o dentro de un grupo específico, como el grupo Administradores, debe establecer el ámbito de la búsqueda para reflejar la circunstancia. Para obtener el mejor rendimiento, debe intentar dirigirse al ámbito para buscar el menor número de objetos posible.

Si no está seguro de dónde se ubicará un objeto en la empresa, puede enlazar al servicio de catálogo global. El servicio de catálogo global contiene una lista de todos los objetos del directorio y un pequeño subconjunto de los atributos de cada objeto. Después de encontrar el objeto en el catálogo global, puede recuperar su nombre distintivo del catálogo global y usarlo para enlazar con el objeto para realizar otras operaciones.

Después de decidir a qué objeto enlazar, puede restringir aún más la consulta a uno de los ámbitos siguientes: una consulta base, una consulta de un nivel o una búsqueda de subárbol, como se muestra en la ilustración siguiente.

![objetos en la raíz de una búsqueda de una búsqueda base, de un nivel o de subárbol](images/netds6.png)

## <a name="base"></a>Base

Una consulta base limita la búsqueda solo al objeto base. El número máximo de objetos devueltos siempre es uno. Esta búsqueda se puede usar para comprobar la existencia de un objeto . Por ejemplo, si tiene el nombre distintivo de un objeto y debe comprobar la existencia del objeto en función de la ruta de acceso, puede usar una búsqueda de un nivel. Si se produce un error en la búsqueda, puede suponer que es posible que se haya cambiado el nombre del objeto o que se haya movido a otra ubicación, o que se le han dado datos incorrectos sobre el objeto. Tenga en cuenta que debe almacenar el GUID en lugar del nombre distintivo si desea volver a visitar un objeto. Esto permite cambiar el nombre del objeto o moverlo en la jerarquía de directorios sin que se rompa el vínculo persistente.

## <a name="one-level"></a>Un nivel

Una búsqueda de un nivel está restringida a los secundarios inmediatos de un objeto base, pero excluye el propio objeto base. Esta configuración puede realizar una búsqueda de destino de objetos secundarios inmediatos de un objeto primario. Por ejemplo, si tiene un objeto primario denominado P1 y sus elementos secundarios inmediatos son: C1, C2, C3, en una búsqueda de un nivel, se debe incluir C1, C2 y C3 al evaluar los criterios, pero P1 no formaría parte de la búsqueda. Se puede usar una búsqueda de un nivel para enumerar todos los elementos secundarios de un objeto. De hecho, en algunos proveedores adsi, la enumeración [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) se traduce en una búsqueda de un nivel.

## <a name="subtree"></a>Subárbol

Una búsqueda de subárbol, también conocida como búsqueda profunda, incluye todos los objetos debajo del objeto base, excepto el propio objeto base. Esta búsqueda puede generar referencias a otros servidores. Esta búsqueda tiene el mayor ámbito y puede devolver un conjunto de resultados grande. Si es posible, busque al menos un atributo indexado y establezca la configuración de referencias (para obtener más información, vea Rendimiento y control de conjuntos de resultados [grandes)](performance-and-handling-large-result-sets.md)para que coincidan con los requisitos de búsqueda. También se sugiere que los resultados de una búsqueda de subárbol se realicen de forma asincrónica y se paginan para reducir la sobrecarga del servidor y la eficacia de la red. Normalmente, una búsqueda de subárbol se usa para buscar objetos en un ámbito determinado. Por ejemplo, busque todos los usuarios con cuentas que expirarán en 30 días o menos.

 

 




