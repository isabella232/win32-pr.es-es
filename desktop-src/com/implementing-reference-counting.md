---
title: Implementar el recuento de referencias
description: Implementar el recuento de referencias
ms.assetid: d4fd98c9-afa4-4c5c-a3c9-44d34881cbdb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa2a3e9827d35d07fa88b62c6f1097fcb3ad3ae3b5b75764deeac1c9c271050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048163"
---
# <a name="implementing-reference-counting"></a>Implementar el recuento de referencias

El recuento de referencias requiere trabajo por parte del implementador de una clase y de los clientes que usan objetos de esa clase. Al implementar una clase, debe implementar los métodos [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) como parte de la [**interfaz IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Estos dos métodos tienen las siguientes implementaciones sencillas:

-   [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa el recuento de referencias internas del objeto.
-   [**La**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) versión disminuye primero el recuento de referencias internas del objeto y, a continuación, comprueba si el recuento de referencias ha disminuido a cero. Si lo ha hecho, significa que ya no se usa el objeto, por lo que la **función Release** desasigne el objeto.

Un enfoque de implementación común para la mayoría de los objetos es tener solo una implementación de estos métodos (junto con [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))), que se comparte entre todas las interfaces y, por tanto, un recuento de referencias que se aplica a todo el objeto. Sin embargo, desde la perspectiva de un cliente, el recuento de referencias es estricta y claramente una noción de puntero por interfaz y, por tanto, se pueden implementar objetos que aprovechan esta funcionalidad mediante la construcción dinámica, destrucción, carga o descarga de partes de su funcionalidad basadas en los punteros de interfaz existentes actualmente. Se denominan coloquialmente *interfaces de desmontado.*

Cada vez que un cliente llama a un método (o función de API), como [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), que devuelve un nuevo puntero de interfaz, el método al que se llama es responsable de incrementar el recuento de referencias a través del puntero devuelto. Por ejemplo, cuando un cliente crea por primera vez un objeto, recibe un puntero de interfaz a un objeto que, desde el punto de vista del cliente, tiene un recuento de referencias de uno. Si el cliente llama a [**AddRef en**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) el puntero de interfaz, el recuento de referencias se convierte en dos. El cliente debe llamar a [**Release dos**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) veces en el puntero de interfaz para quitar todas sus referencias al objeto .

Un ejemplo de cómo los recuentos de referencias son estrictamente por puntero de interfaz se produce cuando un cliente llama a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en el primer puntero para una nueva interfaz o la misma interfaz. En cualquiera de estos casos, el cliente debe llamar a [**Release una**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) vez para cada puntero. COM no requiere que un objeto devuelva el mismo puntero cuando se le pida la misma interfaz varias veces. (La única excepción a esto es una consulta a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), que identifica un objeto a COM). Esto permite que la implementación del objeto administre los recursos de forma eficaz.

La seguridad de subprocesos también es un problema importante a la hora de implementar [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Para obtener más información, [vea Procesos, subprocesos y departamentos](processes--threads--and-apartments.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de duraciones de objetos mediante el recuento de referencias](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 