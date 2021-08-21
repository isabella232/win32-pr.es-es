---
title: Método SetInfo
description: El método SetInfo de los IADs guarda los valores actuales de las propiedades de este objeto Active Directory de la caché de propiedades en el almacén de directorios subyacente. Esto es análogo a vaciar un búfer en el disco.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- SetInfo ADSI ,using
- adsi de propiedades, guardar los valores actuales de las propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e732cefa2d09b92f4fefec2b56f5f2ac8a99f77b2c7720822173cfaa647d7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023143"
---
# <a name="the-setinfo-method"></a>Método SetInfo

El [**método IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) guarda los valores actuales de las propiedades de este objeto Active Directory de la caché de propiedades en el almacén de directorios subyacente. Esto es análogo a vaciar un búfer en el disco.

[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) actualiza los objetos que ya existen en el directorio o crea una nueva entrada de directorio para los objetos recién creados.

En el momento de la llamada a [**SetInfo,**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) si se han escrito valores de caché de propiedades con un código de control [**PutEx,**](/windows/desktop/api/Iads/nf-iads-iads-putex) como ADS PROPERTY UPDATE o ADS PROPERTY CLEAR, las solicitudes adecuadas se pasan al servicio de directorio \_ \_ \_ \_ subyacente.

 

 




