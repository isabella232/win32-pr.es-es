---
description: Puede instalar ensamblados en paralelo como ensamblados compartidos o como ensamblados privados. Para obtener más información, vea Instalar ensamblados en paralelo como ensamblados privados e instalar ensamblados en paralelo como ensamblados compartidos.
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Instalar ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be68580c7f0e3890c2e53b148daec92fbad18ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497231"
---
# <a name="installing-side-by-side-assemblies"></a>Instalar ensamblados en paralelo

Puede instalar ensamblados en paralelo como [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies) o como [ensamblados privados](/windows/desktop/Msi/private-assemblies). Para obtener más información, vea [Instalar ensamblados en paralelo como ensamblados privados](installing-side-by-side-assemblies-as-private-assemblies.md) e [Instalar ensamblados en paralelo como ensamblados compartidos](installing-side-by-side-assemblies-as-shared-assemblies.md).

Observe lo siguiente:

-   Los ensamblados instalados en la caché global de ensamblados mediante una instalación de mediante el [contexto de instalación](/windows/desktop/Msi/installation-context) por usuario no están protegidos por protección de archivos de Windows.
-   Los ensamblados que se instalan en la caché global de ensamblados mediante una instalación de mediante el [contexto de instalación](/windows/desktop/Msi/installation-context) por equipo están protegidos por protección de archivos de Windows.

 

 
