---
title: Instalación desde un CD en línea
description: Instalación desde un CD en línea
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Reproductor de Windows Media en línea, instalar desde CD mientras está en línea
- tiendas en línea, instalación desde CD mientras está en línea
- tiendas en línea de tipo 1, instalación desde CD mientras está en línea
- tiendas en línea de tipo 2, instalación desde CD mientras está en línea
- Reproductor de Windows Media tiendas en línea, instalación en línea desde CD
- tiendas en línea, instalación en línea desde CD
- tiendas en línea de tipo 1, instalación en línea desde CD
- tiendas en línea de tipo 2, instalación en línea desde CD
- Reproductor de Windows Media en línea, CD se instala mientras está en línea
- tiendas en línea, instalación de CD mientras está en línea
- tiendas en línea de tipo 1, CD se instala mientras está en línea
- tiendas en línea de tipo 2, CD se instala mientras está en línea
- instalación de tiendas en línea desde CD mientras está en línea
- Instalación de CD de tiendas en línea mientras está en línea
- instalación en línea de tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13589d7ba6dea0693acaacb5e0d1f551b4a4f178c4ccb50a1bd8ebb513dda3de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996515"
---
# <a name="installing-from-a-cd-while-online"></a>Instalación desde un CD en línea

Los usuarios pueden Reproductor de Windows Media desde un CD mientras están conectados a Internet. Cuando esto sucede, Reproductor de Windows Media programa de instalación busca el documento ServiceInfo especificado por el parámetro de línea de comandos *ServiceInfo.* Si el **atributo Key** coincide con el parámetro de línea de comandos *DefaultService,* el programa de instalación inspecciona el elemento Install para personalizar el proceso de instalación. Con los valores de atributo, el programa de instalación muestra el Contrato de licencia del usuario final (CLUF) y la declaración de privacidad, y también recupera e instala el archivo .cab en el equipo del usuario. Por ejemplo, puede usar esta característica para instalar la versión más reciente de un objeto COM que requiere la tienda en línea.

Una vez instalado, Reproductor de Windows Media el almacén en línea inicial con el nombre de clave especificado para el parámetro de línea de comandos *DefaultService.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común a los almacenes en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento Install**](install-element.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Establecimiento de la tienda en línea inicial**](setting-the-initial-online-store.md)
</dt> <dt>

[**Configuración de parámetros de línea de comandos para almacenes en línea**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




