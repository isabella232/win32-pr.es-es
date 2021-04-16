---
title: Compilar el complemento para una tienda en línea de tipo 1
description: Compilar el complemento para una tienda en línea de tipo 1
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player tiendas en línea, Complementos
- tiendas en línea, Complementos
- tipo 1 tiendas en línea, Complementos
- Windows Media Player tiendas en línea, generar complementos
- tiendas en línea, crear complementos
- Escriba 1 almacenes en línea, compilando complementos
- Windows Media Player tiendas en línea, interfaz IWMPContentPartner
- tiendas en línea, interfaz IWMPContentPartner
- tipo 1 tiendas en línea, interfaz IWMPContentPartner
- complementos, Windows Media Player tiendas en línea
- complementos, tiendas en línea
- complementos, escriba 1 tiendas en línea
- complementos, interfaz IWMPContentPartner
- complementos, compilar
- Complementos de Windows Media Player, escriba 1 tiendas en línea
- Complementos de Windows Media Player, tiendas en línea
- Complementos de Windows Media Player, Windows Media Player tiendas en línea
- Complementos de Media Player de Windows, interfaz IWMPContentPartner
- Complementos de Windows Media Player, compilar
- IWMPContentPartner
- crear complementos, tipo 1 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695560"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a>Compilar el complemento para una tienda en línea de tipo 1

Una tienda en línea de tipo 1 debe proporcionar un complemento que implemente la interfaz [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . El complemento se ejecuta en un proceso independiente del Media Player de Windows.

Los pasos para crear un complemento que se ejecuta fuera de proceso son los siguientes:

1.  Escriba el complemento como si fuera un servidor COM en proceso.
2.  Cree una entrada del registro **DllSurrogate** en el equipo del usuario. La entrada **DllSurrogate** informa al tiempo de ejecución de com que el complemento debe crearse en una instancia del suplente de dll predeterminado, dllhost.exe.

Para obtener información detallada sobre cómo registrar el complemento, consulte [claves del registro y entradas para una tienda en línea de tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).

No es necesario crear ningún código auxiliar o proxy para el complemento. Toda la compatibilidad con la serialización la proporciona Windows Media Player.

Puede usar el Asistente para complementos de tienda en línea para crear rápidamente un complemento que sirve como punto de partida. Para obtener más información, consulte [instalar el complemento de la tienda en línea](installing-the-online-store-plug-in-wizard.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para las tiendas en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




