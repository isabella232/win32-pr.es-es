---
title: Objetos de almacenamiento y de secuencia para un conjunto de propiedades
description: El programador especifica si un conjunto de propiedades se almacena en un almacenamiento o en una secuencia cuando se crea el conjunto de propiedades.
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4ebd5d03c3b17e02aa47a7a859576b4cc04607a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104078525"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a>Objetos de almacenamiento y de secuencia para un conjunto de propiedades

El programador especifica si un conjunto de propiedades se almacena en un almacenamiento o en una secuencia cuando se crea el conjunto de propiedades. El \_ valor de enumeración PROPSETFLAG no simple, pasado en el parámetro *grfFlags* al método [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) , indica esto. La configuración donde se almacena el conjunto de propiedades proporciona controles de aplicación adecuados para interoperar completamente a través de la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) con el conjunto de propiedades com.

Si \_ se establece la marca PROPSETFLAG nonsimple, el conjunto de propiedades se almacena en un objeto de almacenamiento y se pueden escribir valores de propiedad no simples en él. Los valores no simples incluyen valores con un valor **VARTYPE** de \_ almacenamiento VT, \_ flujo VT, \_ objeto almacenado VT \_ o \_ objeto VT Streamed \_ . Para obtener más información sobre los valores de **VARTYPE** y cómo usarlos, consulte la estructura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Si \_ no se establece la marca PROPSETFLAG nonsimple, solo se pueden escribir valores simples en el conjunto de propiedades.

En el objeto de almacenamiento de un conjunto de propiedades no simples, se crea una secuencia denominada Contents. Este es el flujo principal del conjunto de propiedades y contiene todos los valores de propiedad sencillos. Los valores de propiedad no simples (secuencias y almacenamientos) se almacenan en el objeto de almacenamiento principal del conjunto de propiedades como subflujos y almacenamientos. Es decir, estos valores no simples se almacenan como elementos del mismo nivel en la secuencia de contenido. El nombre de las secuencias y almacenamientos del mismo nivel viene determinado por la implementación de y se almacena en el flujo de contenido de forma similar a como se almacena una propiedad de cadena simple.

 

 