---
title: Contención y delegación
description: El mecanismo más común para reutilizar objetos en COM es la contención o delegación.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2d90d3439bcb9fb6038940d860533a090ac68fbdee6ca9b2a832afb2803d03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678865"
---
# <a name="containmentdelegation"></a>Contención y delegación

El mecanismo más común para la reutilización de objetos en COM es *la contención o delegación.* Este tipo de reutilización es un concepto conocido que se encuentra en la mayoría de los sistemas y lenguajes orientados a objetos. El objeto externo, que debe usar el objeto interno, actúa como un cliente de objeto para el objeto interno. El objeto externo "contiene" el objeto interno y, cuando el objeto externo requiere los servicios del objeto interno, el objeto externo delega explícitamente la implementación en los métodos del objeto interno. Es decir, el objeto externo usa los servicios del objeto interno para implementarse.

No es necesario que los objetos externos e internos admitan las mismas interfaces, aunque ciertamente es razonable contener un objeto que implementa una interfaz que el objeto externo no tiene e implementar los métodos del objeto externo simplemente como llamadas a los métodos correspondientes en el objeto interno. Sin embargo, cuando la complejidad de los objetos externos e internos difiere mucho, el objeto externo puede implementar algunos de los métodos de sus interfaces delegando llamadas a métodos de interfaz implementados en el objeto interno.

Es fácil implementar la contención para un objeto externo. El objeto externo crea los objetos internos que debe usar como lo haría cualquier otro cliente. Esto no es nada nuevo: el proceso es como un objeto de C++ que contiene un objeto de cadena de C++ que usa para realizar determinadas funciones de cadena, incluso si el objeto externo no se considera un objeto de cadena por sí mismo. A continuación, con su puntero al objeto interno, una llamada a un método del objeto externo genera una llamada a un método de objeto interno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agregación](aggregation.md)
</dt> </dl>

 

 




