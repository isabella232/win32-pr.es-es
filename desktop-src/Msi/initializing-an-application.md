---
description: Para habilitar la funcionalidad del instalador, una aplicación debe llamar a varias funciones cuando se está inicializando.
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: Inicialización de una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171814"
---
# <a name="initializing-an-application"></a>Inicialización de una aplicación

Para habilitar la funcionalidad del instalador, una aplicación debe llamar a varias funciones cuando se está inicializando. Para obtener más información, vea [Mecanismo de instalación](installation-mechanism.md). En los pasos siguientes se describe cómo usar el instalador para inicializar una aplicación:

**Para inicializar una aplicación**

1.  Llame a [**la función MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) para que la aplicación pueda identificarse en el instalador.

    El código de producto es un parámetro necesario para muchas funciones del instalador.

2.  Llame a [**la función MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) para recopilar información del usuario la primera vez que se inicia la aplicación.

    Si se produce un error en la llamada a [**MsiGetUserInfo,**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) llame a la [**función MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) para recopilar información del usuario.

3.  Muestre una interfaz de usuario predeterminada, si es necesario, llamando a la [**función MsiSetInternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

    Para crear su propia interfaz de usuario, regístrela con el instalador mediante una llamada a la [**función MsiSetExternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)

4.  Llame a [**la función MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) para establecer el nivel de registro.
5.  Presente al usuario las características disponibles enumerando las características de la aplicación. Puede enumerar las características de las siguientes maneras:
    -   Consulte el instalador característica por característica. Por ejemplo, antes de que la aplicación dibuje un botón o un elemento de menú, la aplicación llama a la función [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) para que el instalador pueda comprobar que la característica está disponible.
    -   Para enumerar todas las características disponibles a la vez, llame a [**la función MsiEnumFeatures.**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) Para usar esta función, la aplicación debe llamar a **MsiEnumFeatures** repetidamente al incrementar un índice.
6.  Obtenga información detallada sobre la instalación actual llamando varias veces a las siguientes funciones de enumeración, incrementando una variable de índice para cada llamada:

    -   Llame a [**la función MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) para enumerar los productos registrados con el instalador.
    -   Llame a [**la función MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) para enumerar los componentes.
    -   Llame a [**la función MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) para enumerar los calificadores de componente.
    -   Llame a [**la función MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) para enumerar los productos de un componente determinado.

    Si el valor devuelto en una función de enumeración es ERROR SUCCESS, todavía hay más elementos que enumerar y se debe llamar de nuevo a la función con una variable de \_ índice incrementado. Si el valor devuelto es ERROR NO MORE ITEMS, se han enumerado todos los elementos y no se debe volver a llamar \_ \_ a la \_ función.

 

 



