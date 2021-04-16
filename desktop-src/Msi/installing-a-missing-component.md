---
description: Puede usar la Windows Installer para detectar los componentes o archivos que faltan y, a continuación, volver a instalar las características que contienen los componentes que faltan.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Instalación de un componente que falta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652583"
---
# <a name="installing-a-missing-component"></a>Instalación de un componente que falta

Puede usar la Windows Installer para detectar los componentes o archivos que faltan y, a continuación, volver a instalar las características que contienen los componentes que faltan. Dado que el instalador instala las características de y no los componentes de, primero debe resolver el componente al que pertenece un archivo que falta y, a continuación, instalar la característica que contiene el componente. Si hay más de una característica vinculada al componente, el instalador instala la característica que requiere menos espacio en disco.

Si llama a [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), puede comprobar que el archivo de clave de un componente está presente. Sin embargo, aún es posible que falten otros archivos que pertenecen al componente. En ese escenario, llame a [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea). A continuación, el instalador se resuelve como el componente al que pertenece el archivo e instala la característica que está vinculada al componente que requiere menos espacio en disco.

Si se produce un error inesperado en la función [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) , debe instalar los componentes que falten.

En el procedimiento siguiente se muestra cómo instalar los componentes que faltan.

**Para detectar e instalar un componente que falta**

1.  Llame a [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) para comprobar que el archivo de clave de un componente está presente. Sin embargo, incluso si el archivo de clave del componente está presente, aún es posible que falten otros archivos que pertenecen al componente.
2.  Llame a la función [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) si se desconoce la característica asociada al componente.
3.  Llame a la función [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) o [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) si se conoce la característica asociada al componente.
4.  Llame a [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) si una aplicación no puede abrir un archivo.

 

 



