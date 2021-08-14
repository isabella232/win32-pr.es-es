---
title: Enumeración de particiones de directorio de aplicación en un bosque
description: Al igual que las particiones de dominio, cada partición de directorio de aplicación se representa mediante un objeto crossRef en el contenedor Particiones de la partición de configuración.
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- Enumeración de particiones de directorio de aplicación en un bosque de AD
- Application Directory Partitions AD , Enumerating in a Forest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4e8d48b2fc93ad7a879f76f2bbaa130186706ef957320612c866cb3b9f892c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191372"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>Enumeración de particiones de directorio de aplicación en un bosque

Al igual que las particiones de dominio, cada partición de directorio de aplicación se representa mediante un [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) en el contenedor Particiones de la partición de configuración. Cada **objeto crossRef** almacena datos sobre su partición correspondiente.

Un [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) que representa una partición de dominio se distingue de un objeto **crossRef** que representa una partición de directorio de aplicación por el contenido del [**atributo systemFlags.**](/windows/desktop/ADSchema/a-systemflags) El **objeto crossRef** que representa una partición de dominio tendrá las marcas [**ADS \_ SYSTEMFLAG CR \_ \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) y **ADS \_ SYSTEMFLAG CR \_ \_ NTDS \_ DOMAIN** establecidas en el **atributo systemFlags.** El **objeto crossRef** que representa una partición de directorio de aplicación tendrá establecida la marca DE NC ADS **\_ SYSTEMFLAG CR \_ \_ NTDS \_** y la marca DE DOMINIO **\_ \_ \_ NTDS \_ DE ADS SYSTEMFLAG CR** no se establecerá en el atributo **systemFlags.**

Los objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representan las particiones Esquema y Configuración también tendrán la marca DE NC ADS SYSTEMFLAG CR NTDS establecida y la marca DE DOMINIO [**\_ \_ \_ \_ NTDS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) **DE ADS \_ SYSTEMFLAG \_ CR \_ \_** no se establecerá en el [**atributo systemFlags.**](/windows/desktop/ADSchema/a-systemflags) Esto requiere que estos dos **objetos crossRef** se distinga por el contenido del [**atributo nCName.**](/windows/desktop/ADSchema/a-ncname) El **atributo nCName** del objeto **crossRef** que representa el contenedor Schema será idéntico al atributo **schemaNamingContext** del objeto RootDSE. De forma similar, el atributo **nCName** para el objeto **crossRef** que representa el contenedor Configuration será idéntico al atributo **configurationNamingContext** del objeto RootDSE.

**Para identificar todas las particiones de directorio de aplicación de un bosque, realice los pasos siguientes**

1.  En el contenedor Particiones de la partición de configuración, busque o enumere todos los [**objetos crossRef.**](/windows/desktop/ADSchema/c-crossref)
2.  Si un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) no tiene la marca ADS [**\_ SYSTEMFLAG \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) establecida o tiene la marca DE DOMINIO **\_ \_ \_ NTDS \_ SYSTEMFLAG CR** de ADS establecida en el valor del atributo [**systemFlags,**](/windows/desktop/ADSchema/a-systemflags) excluya el objeto del conjunto de resultados.
3.  Excluya la partición Schema del conjunto de resultados comparando el atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con el atributo **schemaNamingContext** del objeto RootDSE.
4.  Excluya la partición Configuration del conjunto de resultados comparando el atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con el atributo **configurationNamingContext** del objeto RootDSE.
5.  El resto de [**objetos crossRef**](/windows/desktop/ADSchema/c-crossref) del conjunto de resultados representan particiones de directorio de aplicación.

 

 