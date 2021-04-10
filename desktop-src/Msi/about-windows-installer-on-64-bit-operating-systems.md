---
description: Windows Installer se ejecuta como un servicio en equipos que usan Windows de 32 bits o de 64 bits.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Acerca de Windows Installer en sistemas operativos de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "104279671"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a>Acerca de Windows Installer en sistemas operativos de 64 bits

Windows Installer se ejecuta como un servicio en equipos que usan Windows de 32 bits o de 64 bits. Las versiones del instalador anteriores a la versión 2,0 solo pueden instalar y administrar paquetes de Windows Installer de 32 bits en sistemas operativos de 32 bits. Tenga en cuenta que no se puede anunciar ni instalar una aplicación de 64 bits en un sistema operativo de 32 bits.

Un paquete de Windows Installer debe especificarse como un paquete de 32 bits o de 64 bits; no se puede especificar como neutral. En un equipo que utiliza un sistema operativo de 64 bits, el servicio Windows Installer se hospeda en un proceso de 64 bits que instala los paquetes de 32 bits y de 64 bits. Windows Installer instala tres tipos de paquetes de Windows Installer en un equipo que ejecuta un sistema operativo de 64 bits:

-   paquetes de 32 bits que contienen solo componentes de 32 bits.
-   paquetes de 64 bits que contienen algunos componentes de 32 bits.
-   paquetes de 64 bits que contienen solo componentes de 64 bits.

En las secciones siguientes se describen los dos tipos de paquetes de Windows Installer y las nuevas propiedades de instalador proporcionadas por Windows Installer para los paquetes de 64 bits.

[Paquetes de Windows Installer de bits de 32](32-bit-windows-installer-packages.md)

[Paquetes de Windows Installer de bits de 64](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar paquetes de Windows Installer de 64 bits](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



