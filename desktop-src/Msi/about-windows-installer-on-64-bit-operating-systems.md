---
description: Windows El instalador se ejecuta como un servicio en equipos que usan máquinas de 32 o 64 Windows.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Acerca Windows instalador en sistemas operativos de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159250"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a>Acerca Windows instalador en sistemas operativos de 64 bits

Windows El instalador se ejecuta como un servicio en equipos que usan máquinas de 32 o 64 Windows. Las versiones del instalador anteriores a la versión 2.0 pueden instalar y administrar paquetes de instalador de Windows de 32 bits solo en sistemas operativos de 32 bits. Tenga en cuenta que no puede anunciar ni instalar una aplicación de 64 bits en un sistema operativo de 32 bits.

Un Windows installer debe especificarse como un paquete de 32 o 64 bits; no se puede especificar como neutro. En un equipo que usa un sistema operativo de 64 bits, el servicio instalador de Windows se hospeda en un proceso de 64 bits que instala paquetes de 32 y 64 bits. Windows El instalador instala tres tipos de paquetes Windows instalador en un equipo que ejecuta un sistema operativo de 64 bits:

-   Paquetes de 32 bits que contienen solo componentes de 32 bits.
-   Paquetes de 64 bits que contienen algunos componentes de 32 bits.
-   Paquetes de 64 bits que contienen solo componentes de 64 bits.

En las secciones siguientes se describen los dos tipos de paquetes Windows Installer y las nuevas propiedades del instalador proporcionadas por Windows Installer para paquetes de 64 bits.

[Paquetes del instalador de Windows de 32 bits](32-bit-windows-installer-packages.md)

[Paquetes del instalador de Windows de 64 bits](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de paquetes del instalador de Windows de 64 bits](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



