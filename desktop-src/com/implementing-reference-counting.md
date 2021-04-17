---
title: Implementación del recuento de referencias
description: Implementación del recuento de referencias
ms.assetid: d4fd98c9-afa4-4c5c-a3c9-44d34881cbdb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d4dfe2b0faf2fc6557d1b089e33ae6ce4b98cb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714485"
---
# <a name="implementing-reference-counting"></a>Implementación del recuento de referencias

El recuento de referencias requiere trabajo en la parte del implementador de una clase y de los clientes que usan objetos de esa clase. Al implementar una clase, debe implementar los métodos [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) como parte de la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Estos dos métodos tienen las siguientes implementaciones simples:

-   [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa el recuento de referencias internas del objeto.
-   [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) primero disminuye el recuento de referencias interno del objeto y, a continuación, comprueba si el recuento de referencias ha descendido a cero. En caso afirmativo, eso significa que nadie está utilizando el objeto más, por lo que la función **Release** desasigna el objeto.

Un enfoque de implementación común para la mayoría de los objetos es tener solo una implementación de estos métodos (junto con [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))), que se comparte entre todas las interfaces y, por lo tanto, un recuento de referencias que se aplica a todo el objeto. Sin embargo, desde el punto de vista de un cliente, el recuento de referencias es estrictamente y claramente una noción por puntero a interfaz y, por tanto, los objetos que aprovechan esta funcionalidad mediante la construcción, destrucción, carga o descarga de partes de su funcionalidad en función de los punteros de interfaz que se pueden implementar actualmente. Se trata de suele denominados *interfaces de recorte*.

Cada vez que un cliente llama a un método (o una función de API), como [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), que devuelve un nuevo puntero de interfaz, el método al que se llama es responsable de incrementar el recuento de referencias a través del puntero devuelto. Por ejemplo, cuando un cliente crea primero un objeto, recibe un puntero de interfaz a un objeto que, desde el punto de vista del cliente, tiene un recuento de referencias de uno. Si el cliente llama a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en el puntero de interfaz, el recuento de referencias se convierte en dos. El cliente debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) dos veces en el puntero de interfaz para quitar todas sus referencias al objeto.

Un ejemplo de cómo los recuentos de referencias son estrictamente por interfaz: puntero se produce cuando un cliente llama a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en el primer puntero para una nueva interfaz o la misma interfaz. En cualquiera de estos casos, el cliente debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) una vez para cada puntero. COM no requiere que un objeto devuelva el mismo puntero cuando se le pida varias veces la misma interfaz. (La única excepción a esto es una consulta a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), que identifica un objeto a com). Esto permite que la implementación del objeto administre los recursos de forma eficaz.

La seguridad para subprocesos también es un problema importante en la implementación de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Para obtener más información, consulte [procesos, subprocesos y apartamentos](processes--threads--and-apartments.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar la duración de los objetos mediante el recuento de referencias](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 