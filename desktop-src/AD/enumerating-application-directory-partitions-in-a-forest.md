---
title: Enumerar particiones de directorio de aplicaciones en un bosque
description: Al igual que las particiones de dominio, todas las particiones de directorio de aplicaciones se representan mediante un objeto crossRef en el contenedor de particiones de la partición de configuración.
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- Enumerar particiones de directorio de aplicaciones en un bosque de AD
- Particiones de directorio de aplicaciones AD, enumeración en un bosque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d42bbe28ef37932394721d0c234ba3970ac263b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077523"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>Enumerar particiones de directorio de aplicaciones en un bosque

Al igual que las particiones de dominio, todas las particiones de directorio de aplicaciones se representan mediante un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) en el contenedor de particiones de la partición de configuración. Cada objeto **crossRef** almacena datos sobre su partición correspondiente.

Un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa una partición de dominio se distingue de un objeto **crossRef** que representa una partición de directorio de aplicaciones por el contenido del atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) . El objeto **crossRef** que representa una partición de dominio tendrá las marcas de dominio [**ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) y **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_** en el atributo **systemFlags** . El objeto **crossRef** que representa una partición de directorio de aplicación tendrá la marca **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ NC** establecida y la marca **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ Domain** no se establecerá en el atributo **systemFlags** .

Los objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representan el esquema y las particiones de configuración también tendrán establecida la marca tiene el marcador de [**\_ CN ad SYSTEMFLAG \_ CR \_ NTDS \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) y el marcador **ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ Domain** no se establecerá en el atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) . Esto requiere que estos dos objetos **crossRef** se contingan por el contenido del atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) . El atributo **NCName** del objeto **crossRef** que representa el contenedor de esquema será idéntico al atributo **schemaNamingContext** del objeto RootDSE. Del mismo modo, el atributo **NCName** del objeto **crossRef** que representa el contenedor de configuración será idéntico al atributo **configurationNamingContext** del objeto RootDSE.

**Para identificar todas las particiones de directorio de aplicaciones de un bosque, siga estos pasos:**

1.  En el contenedor particiones de la partición de configuración, busque o Enumere todos los objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) .
2.  Si un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) no tiene establecida la marca [**ADS \_ SYSTEMFLAG \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) o tiene la marca de **\_ dominio ADS SYSTEMFLAG \_ CR \_ NTDS \_** establecida en el valor del atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , excluya el objeto del conjunto de resultados.
3.  Excluya la partición de esquema del conjunto de resultados comparando el atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con el atributo **schemaNamingContext** del objeto RootDSE.
4.  Excluya la partición de configuración del conjunto de resultados comparando el atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con el atributo **configurationNamingContext** del objeto RootDSE.
5.  Los objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) restantes del conjunto de resultados representan particiones de directorio de aplicaciones.

 

 