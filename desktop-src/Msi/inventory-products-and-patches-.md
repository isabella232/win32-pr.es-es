---
description: 'Los usuarios y las aplicaciones con privilegios administrativos pueden utilizar funciones de Windows Installer para realizar un inventario de las aplicaciones, características, componentes y revisiones de Windows Installer instalados en el sistema. A partir de Windows Installer&\# 160; 3.0, los usuarios y las aplicaciones que tienen privilegios de administrador pueden enumerar las aplicaciones Windows Installer, las características, los componentes y las revisiones instalados en el sistema por todos los usuarios. Los administradores y las aplicaciones pueden obtener información sobre un producto o revisión para un usuario determinado o para todos los usuarios del sistema. Las aplicaciones pueden obtener el estado de las características o el estado de los componentes de un usuario determinado. Las funciones de inventario disponibles a partir de Windows Installer&\# 160; 3.0 pueden limitar el ámbito de los elementos que se van a buscar por contexto de instalación y contexto de usuario. Existen tres contextos de instalación posibles: por usuario, por equipo y por usuario administrado. El contexto de usuario puede ser un usuario determinado o todos los usuarios del sistema. Las versiones de las funciones de inventario de Windows Installer anteriores a Windows Installer&\# 160; 3.0 solo pueden enumerar los elementos instalados en el sistema en el contexto de la máquina o en el contexto por usuario del usuario actual. Esta limitación evita un inventario completo de todos los Windows Installer los productos y revisiones instalados en el sistema por parte de usuarios que no sean el usuario actual. Enumerar ProductsEnumerating PatchesObtaining Product InformationObtaining patch InformationObtaining Component State InformationObtaining Feature State Information'
ms.assetid: ef95c3c8-b4c8-4305-8aa2-07ec74b3121b
title: Uso de Windows Installer para inventariar productos y revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7915a8a58954c2e07a3dae9536ed7bae399e416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540243"
---
# <a name="using-windows-installer-to-inventory-products-and-patches"></a>Uso de Windows Installer para inventariar productos y revisiones

Los usuarios y las aplicaciones con privilegios administrativos pueden utilizar funciones de Windows Installer para realizar un inventario de las aplicaciones, características, componentes y revisiones de Windows Installer instalados en el sistema.

A partir de Windows Installer 3,0, los usuarios y las aplicaciones que tienen privilegios de administrador pueden enumerar las aplicaciones, las características, los componentes y las revisiones de Windows Installer instalados en el sistema por todos los usuarios. Los administradores y las aplicaciones pueden obtener información sobre un producto o revisión para un usuario determinado o para todos los usuarios del sistema. Las aplicaciones pueden obtener el estado de las características o el estado de los componentes de un usuario determinado.

Las funciones de inventario disponibles a partir de Windows Installer 3,0 pueden limitar el ámbito de los elementos que se van a buscar por contexto de instalación y contexto de usuario. Existen tres contextos de instalación posibles: por usuario, por equipo y por usuario administrado. El contexto de usuario puede ser un usuario determinado o todos los usuarios del sistema.

Las versiones de las funciones de inventario de Windows Installer anteriores a Windows Installer 3,0 solo pueden enumerar los elementos instalados en el sistema en el contexto de la máquina o en el contexto por usuario del usuario actual. Esta limitación evita un inventario completo de todos los Windows Installer los productos y revisiones instalados en el sistema por parte de usuarios que no sean el usuario actual.

-   [Enumerar productos](#enumerating-products)
-   [Enumerar revisiones](#enumerating-patches)
-   [Obtención de información del producto](#obtaining-product-information)
-   [Obtención de información de revisión](#obtaining-patch-information)
-   [Obtención de información de estado de componentes](#obtaining-component-state-information)
-   [Obtención de información de estado de características](#obtaining-feature-state-information)

## <a name="enumerating-products"></a>Enumerar productos

Utilice la función [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para enumerar Windows Installer aplicaciones instaladas en el sistema. Esta función puede encontrar todas las instalaciones por equipo y las instalaciones por usuario de las aplicaciones (administradas y no administradas) del usuario actual y de otros usuarios del sistema. Use el parámetro *dwContext* para especificar el contexto de instalación que se va a buscar. Puede especificar cualquiera de las combinaciones de los contextos de instalación posibles o cualquier combinación de ellos. Use el parámetro *szUserSid* para especificar el contexto de usuario de las aplicaciones que se van a buscar.

## <a name="enumerating-patches"></a>Enumerar revisiones

Utilice la función [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) para buscar las revisiones aplicadas para una aplicación. Esta función puede buscar revisiones aplicadas para una aplicación determinada o para todas las aplicaciones del sistema. Esta función puede encontrar las revisiones que se aplican a todas las instalaciones por equipo y a las instalaciones por usuario de las aplicaciones (administradas y no administradas) del usuario actual y de otros usuarios del sistema.

Puede usar el contexto de instalación y el contexto de usuario para restringir la enumeración de revisiones a un contexto determinado o a través de todos los contextos. Use el parámetro *dwContext* para especificar el contexto de instalación que se va a buscar. Puede especificar cualquiera de las combinaciones de los contextos de instalación posibles o cualquier combinación de ellos. Use el parámetro *szUserSid* para especificar el contexto de usuario de las aplicaciones que se van a buscar.

**Para enumerar las revisiones aplicadas para todos los productos anunciados o instalados por todos los usuarios del sistema**

-   Llame a la función [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) .
    -   Use **null** para el valor del parámetro *szProductCode* .
    -   Use "s-1-1-0" para el valor del parámetro *szUserSid* .
    -   Use "MSIINSTALLCONTEXT \_ All" para el valor del parámetro *dwContext* .

**Para enumerar las revisiones aplicadas para todos los productos anunciados o instalados por todos los usuarios del sistema**

1.  Llame a la función [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) .

    -   Use **null** para el valor del parámetro *szProductCode* .
    -   Use "s-1-1-0" para el valor del parámetro *szUserSid* .
    -   Use "MSIINSTALLCONTEXT \_ All" para el valor del parámetro *dwContext* .

    La función proporciona un código de producto, un contexto de usuario y un contexto de instalación para cada aplicación encontrada.

2.  Para cada aplicación enumerada en el paso 1, llame a [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) para enumerar las revisiones.

    Use los códigos de producto, contextos de usuario y contextos de instalación obtenidos de [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para los valores de *szProductCode*, *szUserSid* y *DwContext*, y cada llamada de función **MsiEnumProductsEx** .

## <a name="obtaining-product-information"></a>Obtención de información del producto

Utilice la función [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) para obtener información sobre las aplicaciones que se anuncian o se instalan en el sistema y las propiedades que se pueden recuperar. Esta función puede obtener información de una instancia de una aplicación instalada en una cuenta de usuario que no sea el usuario actual, pero no puede consultar una instancia de un producto que se anuncie en un contexto no administrado por usuario para una cuenta de usuario que no sea el usuario actual.

Puede especificar el contexto de instalación y el contexto de usuario para restringir la información de las aplicaciones instaladas en un contexto determinado. Use el parámetro *dwContext* para especificar el contexto de instalación que se va a buscar. Solo puede especificar uno de los contextos de instalación posibles. Use el parámetro *szUserSid* para especificar el contexto de usuario de las aplicaciones que se van a buscar.

## <a name="obtaining-patch-information"></a>Obtención de información de revisión

Una aplicación puede llamar a la función [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) para consultar información acerca de la aplicación de una revisión a una instancia especificada de un producto. Se pueden recuperar propiedades como **LocalPackage**, [**transformaciones**](transforms.md)y **State** mediante esta función. No se garantiza que todos los valores de propiedad estén disponibles para las aplicaciones no administradas por usuario si el usuario no ha iniciado sesión actualmente en el equipo. Solo puede especificar uno de los contextos de instalación posibles.

Puede especificar el contexto de instalación y el contexto de usuario para restringir la información a las revisiones aplicadas a las aplicaciones instaladas en un contexto determinado. Use el parámetro *dwContext* para especificar el contexto de instalación que se va a buscar. Solo puede especificar uno de los contextos de instalación posibles. Use el parámetro *szUserSid* para especificar el contexto de usuario de las aplicaciones que se van a buscar.

## <a name="obtaining-component-state-information"></a>Obtención de información de estado de componentes

Las aplicaciones pueden llamar a la función [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea) para obtener el estado instalado de un componente. Esta función determina si el componente está instalado localmente o está instalado para ejecutarse desde el origen. La función puede consultar un componente de una instancia de una aplicación que se instala en cuentas de usuario distintas del usuario actual, siempre que el producto no se anuncie en el contexto no administrado por usuario para una cuenta de usuario que no sea el usuario actual.

Puede especificar un contexto de instalación y un contexto de usuario para obtener el estado de los componentes de las aplicaciones instaladas en un contexto determinado. Use el parámetro *dwContext* para especificar el contexto de instalación que se va a buscar. Solo puede especificar uno de los contextos de instalación posibles. Use el parámetro *szUserSid* para especificar el contexto de usuario de las aplicaciones que se van a buscar.

## <a name="obtaining-feature-state-information"></a>Obtención de información de estado de características

Las aplicaciones pueden llamar a la función [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa) para obtener el estado instalado de una característica del producto. Esta función determina si la característica se anuncia, se instala localmente o se instala para ejecutarse desde el origen. La función se puede usar para consultar cualquier característica de una instancia de una aplicación instalada en la cuenta del equipo o en cualquier contexto de la cuenta de usuario actual o el contexto administrado por usuario en cualquier cuenta de usuario que no sea el usuario actual. Esta función no puede consultar una aplicación instalada en el contexto no administrado por usuario para una cuenta de usuario que no sea el usuario actual. Solo puede especificar uno de los contextos de instalación posibles.

Puede especificar un contexto de instalación y un contexto de usuario para obtener el estado de las características de las aplicaciones instaladas en un contexto determinado. Use el parámetro *dwContext* para especificar el contexto de instalación que se va a buscar. Solo puede especificar uno de los contextos de instalación posibles. Use el parámetro *szUserSid* para especificar el contexto de usuario de las aplicaciones que se van a buscar.

 

 



