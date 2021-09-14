---
description: 'Los usuarios y las aplicaciones con privilegios administrativos pueden usar Windows Installer para realizar un inventario de las aplicaciones, características, componentes y revisiones del instalador de Windows instalados en el sistema. A partir de Windows Installer&160;3.0, todos los usuarios y aplicaciones que tienen privilegios de administrador pueden enumerar las aplicaciones, características, componentes y revisiones del instalador de Windows instalados en el sistema \# por todos los usuarios. Los administradores y las aplicaciones pueden obtener información sobre un producto o revisión para un usuario determinado o para todos los usuarios del sistema. Las aplicaciones pueden obtener el estado de la característica o el estado del componente para un usuario determinado. Las funciones de inventario disponibles a partir de Windows Installer&160;3.0 pueden limitar el ámbito de los elementos que se encuentran en el contexto de instalación y el contexto de \# usuario. Hay tres contextos de instalación posibles: por usuario, por equipo y por usuario administrado. El contexto de usuario puede ser un usuario determinado o todos los usuarios del sistema. Las versiones de las funciones de inventario de Windows Installer anteriores a Windows Installer&160;3.0 solo pueden enumerar los elementos instalados en el sistema en el contexto de la máquina o en el contexto por usuario del \# usuario actual. Esta limitación impide un inventario completo de todos los productos y revisiones Windows Installer instalados en el sistema por usuarios distintos del usuario actual. Enumerar productosEnumerating PatchesObtaining Product InformationObtaining Patch InformationObtaining Component State InformationObtaining Feature State Information'
ms.assetid: ef95c3c8-b4c8-4305-8aa2-07ec74b3121b
title: Usar Windows instalador para inventario de productos y revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7915a8a58954c2e07a3dae9536ed7bae399e416b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072003"
---
# <a name="using-windows-installer-to-inventory-products-and-patches"></a>Usar Windows instalador para inventario de productos y revisiones

Los usuarios y las aplicaciones con privilegios administrativos pueden usar Windows Installer para realizar un inventario de las aplicaciones, características, componentes y revisiones del instalador de Windows instalados en el sistema.

A partir de Windows Installer 3.0, los usuarios y las aplicaciones que tienen privilegios de administrador pueden enumerar las aplicaciones, características, componentes y revisiones del instalador de Windows instalados en el sistema por todos los usuarios. Los administradores y las aplicaciones pueden obtener información sobre un producto o revisión para un usuario determinado o para todos los usuarios del sistema. Las aplicaciones pueden obtener el estado de la característica o el estado del componente para un usuario determinado.

Las funciones de inventario disponibles a partir de Windows Installer 3.0 pueden limitar el ámbito de los elementos que se encuentran en el contexto de instalación y el contexto de usuario. Hay tres contextos de instalación posibles: por usuario, por equipo y por usuario administrado. El contexto de usuario puede ser un usuario determinado o todos los usuarios del sistema.

Las versiones de las funciones de inventario del instalador de Windows anteriores a Windows Installer 3.0 solo pueden enumerar los elementos instalados en el sistema en el contexto del equipo o en el contexto por usuario del usuario actual. Esta limitación impide un inventario completo de todos los productos y revisiones Windows Installer instalados en el sistema por usuarios distintos del usuario actual.

-   [Enumerar productos](#enumerating-products)
-   [Enumerar revisiones](#enumerating-patches)
-   [Obtener información del producto](#obtaining-product-information)
-   [Obtener información de revisión](#obtaining-patch-information)
-   [Obtener información de estado del componente](#obtaining-component-state-information)
-   [Obtener información de estado de características](#obtaining-feature-state-information)

## <a name="enumerating-products"></a>Enumerar productos

Use la [**función MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para enumerar las Windows Installer instaladas en el sistema. Esta función puede encontrar todas las instalaciones por máquina y las instalaciones por usuario de aplicaciones (administradas y no administradas) para el usuario actual y otros usuarios del sistema. Use el *parámetro dwContext* para especificar el contexto de instalación que se va a encontrar. Puede especificar cualquiera o cualquier combinación de los posibles contextos de instalación. Use el *parámetro szUserSid* para especificar el contexto de usuario de las aplicaciones que se va a encontrar.

## <a name="enumerating-patches"></a>Enumerar revisiones

Use la [**función MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) para buscar revisiones aplicadas a una aplicación. Esta función puede buscar revisiones aplicadas a una aplicación determinada o a todas las aplicaciones del sistema. Esta función puede encontrar revisiones aplicadas a todas las instalaciones por máquina y a las instalaciones por usuario de aplicaciones (administradas y no administradas) para el usuario actual y otros usuarios del sistema.

Puede usar el contexto de instalación y el contexto de usuario para restringir la enumeración de revisiones a un contexto determinado o en todos los contextos. Use el *parámetro dwContext* para especificar el contexto de instalación que se va a encontrar. Puede especificar cualquiera o cualquier combinación de los posibles contextos de instalación. Use el *parámetro szUserSid* para especificar el contexto de usuario de las aplicaciones que se va a encontrar.

**Para enumerar las revisiones aplicadas a todos los productos anunciados o instalados por todos los usuarios del sistema**

-   Llame a [**la función MsiEnumPatchesEx.**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
    -   Use **NULL** para el valor del *parámetro szProductCode.*
    -   Use "s-1-1-0" para el valor del *parámetro szUserSid.*
    -   Use "MSIINSTALLCONTEXT \_ ALL" como valor del *parámetro dwContext.*

**Para enumerar las revisiones aplicadas a todos los productos anunciados o instalados por todos los usuarios del sistema**

1.  Llame a [**la función MsiEnumProductsEx.**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)

    -   Use **NULL** para el valor del *parámetro szProductCode.*
    -   Use "s-1-1-0" para el valor del *parámetro szUserSid.*
    -   Use "MSIINSTALLCONTEXT \_ ALL" como valor del *parámetro dwContext.*

    La función proporciona un código de producto, un contexto de usuario y un contexto de instalación para cada aplicación encontrada.

2.  Para cada aplicación enumerada en el paso 1, llame a [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) para enumerar las revisiones.

    Use los códigos de producto, los contextos de usuario y los contextos de instalación obtenidos de [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para los valores *de szProductCode*, *szUserSid* y *dwContext,* y cada llamada de función **MsiEnumProductsEx.**

## <a name="obtaining-product-information"></a>Obtener información del producto

Use la [**función MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) para obtener información sobre las aplicaciones que se anuncian o instalan en el sistema y las propiedades que se pueden recuperar. Esta función puede obtener información de una instancia de una aplicación instalada en una cuenta de usuario que no sea el usuario actual, pero no puede consultar una instancia de un producto que se anuncia en un contexto no administrado por usuario para una cuenta de usuario que no sea el usuario actual.

Puede especificar el contexto de instalación y el contexto de usuario para restringir la información de las aplicaciones instaladas en un contexto determinado. Use el *parámetro dwContext* para especificar el contexto de instalación que se va a encontrar. Solo puede especificar uno de los posibles contextos de instalación. Use el *parámetro szUserSid* para especificar el contexto de usuario de las aplicaciones que se va a encontrar.

## <a name="obtaining-patch-information"></a>Obtener información de revisión

Una aplicación puede llamar a [**la función MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) para consultar información sobre la aplicación de una revisión a una instancia especificada de un producto. Las propiedades como **LocalPackage,** [**Transforms**](transforms.md)y **State** se pueden recuperar mediante esta función. No se garantiza que todos los valores de propiedad estén disponibles para las aplicaciones no administradas por usuario si el usuario no ha iniciado sesión actualmente en la máquina. Solo puede especificar uno de los posibles contextos de instalación.

Puede especificar el contexto de instalación y el contexto de usuario para restringir la información a las revisiones aplicadas a las aplicaciones instaladas en un contexto determinado. Use el *parámetro dwContext* para especificar el contexto de instalación que se va a encontrar. Solo puede especificar uno de los posibles contextos de instalación. Use el *parámetro szUserSid* para especificar el contexto de usuario de las aplicaciones que se va a encontrar.

## <a name="obtaining-component-state-information"></a>Obtener información de estado del componente

Las aplicaciones pueden llamar [**a la función MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea) para obtener el estado instalado de un componente. Esta función determina si el componente se instala localmente o se instala para ejecutarse desde el origen. La función puede consultar un componente de una instancia de una aplicación que se instala en cuentas de usuario que no son el usuario actual, siempre que el producto no se anuncie en el contexto no administrado por usuario para una cuenta de usuario que no sea el usuario actual.

Puede especificar un contexto de instalación y un contexto de usuario para obtener el estado de los componentes de las aplicaciones instaladas en un contexto determinado. Use el *parámetro dwContext* para especificar el contexto de instalación que se va a encontrar. Solo puede especificar uno de los posibles contextos de instalación. Use el *parámetro szUserSid* para especificar el contexto de usuario de las aplicaciones que se va a encontrar.

## <a name="obtaining-feature-state-information"></a>Obtener información de estado de características

Las aplicaciones pueden llamar [**a la función MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa) para obtener el estado instalado de una característica de producto. Esta función determina si la característica se anuncia, se instala localmente o se instala para ejecutarse desde el origen. La función se puede usar para consultar cualquier característica de una instancia de una aplicación instalada en la cuenta de equipo o en cualquier contexto en la cuenta de usuario actual o en el contexto administrado por usuario en cualquier cuenta de usuario que no sea el usuario actual. Esta función no puede consultar una aplicación instalada en el contexto no administrado por usuario para una cuenta de usuario que no sea el usuario actual. Solo puede especificar uno de los posibles contextos de instalación.

Puede especificar un contexto de instalación y un contexto de usuario para obtener el estado de las características de las aplicaciones instaladas en un contexto determinado. Use el *parámetro dwContext* para especificar el contexto de instalación que se va a encontrar. Solo puede especificar uno de los posibles contextos de instalación. Use el *parámetro szUserSid* para especificar el contexto de usuario de las aplicaciones que se va a encontrar.

 

 



