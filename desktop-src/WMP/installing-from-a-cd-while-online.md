---
title: Instalación desde un CD mientras está en línea
description: Instalación desde un CD mientras está en línea
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player tiendas en línea, instalar desde el CD mientras está en línea
- tiendas en línea, instalar desde el CD mientras están en línea
- Escriba 1 tiendas en línea, instalando desde el CD mientras está en línea
- Escriba 2 tiendas en línea, instalando desde el CD mientras está en línea
- Windows Media Player tiendas en línea, instalaciones en línea desde el CD
- tiendas en línea, instalaciones en línea desde el CD
- tipo 1 tiendas en línea, instalaciones en línea desde el CD
- tipo 2 tiendas en línea, instalaciones en línea desde el CD
- Windows Media Player tiendas en línea, CD se instala mientras está en línea
- tiendas en línea, CD se instala en línea
- Escriba 1 tiendas en línea, el CD se instala mientras está en línea
- tipo 2 tiendas en línea, CD se instala mientras está en línea
- instalación de tiendas en línea desde el CD en línea
- CD instala las tiendas en línea mientras están en línea
- instalaciones en línea de tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695360"
---
# <a name="installing-from-a-cd-while-online"></a>Instalación desde un CD mientras está en línea

Los usuarios pueden instalar Windows Media Player desde un CD mientras están conectados a Internet. Cuando esto sucede, el programa de instalación de Windows Media Player localiza el documento ServiceInfo especificado por el parámetro de línea de comandos *ServiceInfo* . Si el atributo **clave** coincide con el parámetro de línea de comandos *DefaultService* , el programa de instalación inspecciona el elemento de instalación para personalizar el proceso de instalación. Con los valores de atributo, el programa de instalación muestra el contrato de licencia para el usuario final (CLUF) y la declaración de privacidad, y también recupera e instala el archivo. cab en el equipo del usuario. Por ejemplo, puede usar esta característica para instalar la versión más reciente de un objeto COM que requiere la tienda en línea.

Una vez instalado, Windows Media Player establece la tienda en línea inicial con el nombre de clave especificado para el parámetro de línea de comandos *DefaultService* .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento install**](install-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Establecimiento de la tienda en línea inicial**](setting-the-initial-online-store.md)
</dt> <dt>

[**Parámetros de la línea de comandos del programa de instalación para tiendas en línea**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




