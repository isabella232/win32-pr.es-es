---
description: Una vez que tenga un identificador de un archivo INF, puede recuperar información de él de varias maneras. Funciones como SetupGetInfInformation, SetupQueryInfFileInformation y SetupQueryInfVersionInformation recuperan información sobre el propio archivo INF.
ms.assetid: e64c9576-ad62-4ebd-8d30-4e4e0da3b8c5
title: Recuperar información de un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cfb1a52fd004b1d812e4a01320a5bdd2bbeca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667517"
---
# <a name="retrieving-information-from-an-inf-file"></a>Recuperar información de un archivo INF

Una vez que tenga un identificador de un archivo INF, puede recuperar información de él de varias maneras. Funciones como [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)y [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) recuperan información sobre el propio archivo INF.

Otras funciones, como [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) y [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) , adquieren información sobre los archivos de origen y los directorios de destino.

Las funciones de bajo nivel como [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) y [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) permiten acceder directamente a la información almacenada en una línea o campo de un archivo INF. Estas funciones son utilizadas internamente por las funciones de nivel superior, pero también están disponibles si necesita tener acceso a la información de INF en el nivel de línea o campo.

 

 



