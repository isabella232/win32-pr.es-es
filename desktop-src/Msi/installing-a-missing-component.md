---
description: Puede usar el instalador de Windows para detectar los componentes o archivos que faltan y, a continuación, volver a instalar las características que contienen los componentes que faltan.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Instalar un componente que falta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e788cad738d46d35a7ac0948be2e2e2d6ede4347eec424fb24cf17571e3a59f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828795"
---
# <a name="installing-a-missing-component"></a>Instalar un componente que falta

Puede usar el instalador de Windows para detectar los componentes o archivos que faltan y, a continuación, volver a instalar las características que contienen los componentes que faltan. Dado que el instalador instala características y no componentes, primero debe resolver a qué componente pertenece un archivo que falta y, a continuación, instalar la característica que contiene el componente. Si hay más de una característica vinculada al componente, el instalador instala la característica que requiere el menor espacio en disco.

Si llama a [**MsiGetComponentPath,**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)puede comprobar que el archivo de clave de un componente está presente. Sin embargo, todavía es posible que falte algún otro archivo que pertenezca al componente. En ese escenario, llame [**a MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea). A continuación, el instalador resuelve al componente al que pertenece el archivo e instala la característica que está vinculada al componente que requiere el menor espacio en disco.

Si se produce un error inesperado en la función [**MsiGetComponentPath,**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) debe instalar los componentes que faltan.

En el procedimiento siguiente se muestra cómo instalar los componentes que faltan.

**Para detectar e instalar un componente que falta**

1.  Llame [**a MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) para comprobar que el archivo de clave de un componente está presente. Sin embargo, incluso si el archivo de clave del componente está presente, todavía es posible que falte otro archivo que pertenezca al componente.
2.  Llame a [**la función MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) si se desconoce la característica asociada al componente.
3.  Llame a [**la función MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) [**o MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) si se conoce la característica asociada al componente.
4.  Llame [**a MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) si una aplicación no puede abrir un archivo.

 

 



