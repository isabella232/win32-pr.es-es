---
title: Creación del complemento para una tienda en línea de tipo 1
description: Creación del complemento para una tienda en línea de tipo 1
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Reproductor de Windows Media en línea, complementos
- tiendas en línea, complementos
- tiendas en línea de tipo 1, complementos
- Reproductor de Windows Media en línea, creación de complementos
- tiendas en línea, creación de complementos
- tiendas en línea de tipo 1, creación de complementos
- Reproductor de Windows Media en línea, interfaz IWMPContentPartner
- online stores,IWMPContentPartner (interfaz)
- type 1 online stores,IWMPContentPartner (interfaz)
- complementos, Reproductor de Windows Media en línea
- complementos, tiendas en línea
- complementos, escriba 1 tienda en línea
- complementos, interfaz IWMPContentPartner
- complementos, compilar
- Reproductor de Windows Media complementos, escriba 1 tienda en línea
- Reproductor de Windows Media complementos,tiendas en línea
- Reproductor de Windows Media complementos, Reproductor de Windows Media tiendas en línea
- Reproductor de Windows Media complementos, interfaz IWMPContentPartner
- Reproductor de Windows Media complementos, compilar
- IWMPContentPartner
- building plug-ins,type 1 online stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fdc5b01a0a8ec526af22e6be90c562524536cdb30b37bd03eb40132af0be49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997855"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a>Creación del complemento para una tienda en línea de tipo 1

Un almacén en línea de tipo 1 debe proporcionar un complemento que implemente la [**interfaz IWMPContentPartner.**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) El complemento se ejecuta en un proceso independiente del Reproductor de Windows Media.

Los pasos para crear un complemento que se ejecuta fuera de proceso son los siguientes:

1.  Escriba el complemento como si fuera un servidor COM en proceso.
2.  Cree una entrada del Registro **DllSurrogate** en el equipo del usuario. La **entrada DllSurrogate** informa al entorno de ejecución COM de que el complemento debe crearse en una instancia del suplente dll predeterminado, dllhost.exe.

Para obtener información detallada sobre cómo registrar el complemento, vea Claves y entradas del Registro [para un almacén en línea de tipo 1.](registry-keys-and-entries-for-a-type-1-online-store.md)

No es necesario crear ningún proxy o código auxiliar para el complemento. Toda la compatibilidad con la serialización la proporciona Reproductor de Windows Media.

Puede usar el Asistente para complementos de tienda en línea para crear rápidamente un complemento que sirva como punto de partida. Para obtener más información, vea [Installing the Online Store Plug-in Wizard](installing-the-online-store-plug-in-wizard.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para almacenes en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




