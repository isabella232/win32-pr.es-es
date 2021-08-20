---
title: Tipo de archivo y modelo de asociaciones de URI
description: Tipo de archivo y modelo de asociaciones de URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabcdb40bd38aeee24ee0e5d86f11651633a7eead1748810e8c1c6a846827690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028863"
---
# <a name="file-type-and-uri-associations-model"></a>Tipo de archivo y modelo de asociaciones de URI

## <a name="platforms"></a>Plataformas

 **Clientes:** Windows 8  
**Servidores:** Windows Server 2012  



## <a name="description"></a>Descripción

El tipo de archivo y el modelo de asociación de URI han cambiado en Windows 8. Las aplicaciones ya no pueden establecerse mediante programación como controlador predeterminado para un tipo de archivo o URI. En su lugar, ahora el usuario siempre controla cuál es el controlador predeterminado para un tipo de archivo o esquema uri.

## <a name="manifestation"></a>Manifestación

La forma en que se presenta este cambio al usuario depende de cómo se diseñe la aplicación, por ejemplo:

-   Muchas aplicaciones comprueban si son el valor predeterminado cada vez que se ejecutan y, si no lo están, solicitan al usuario que las establezca como predeterminadas. Sin embargo, dado que las aplicaciones ya no pueden consultar con precisión para determinar qué aplicación es el controlador predeterminado para un tipo de archivo o esquema uri, ninguna de estas operaciones funciona.
-   Muchas aplicaciones tienen un cuadro de diálogo o un menú integrados o en su instalador que especifica los tipos de archivo para los que la aplicación debe actuar como valor predeterminado. Sin embargo, dado que las aplicaciones ya no pueden establecerse mediante programación como controlador predeterminado para un tipo de archivo o esquema uri, esto ya no funciona.

## <a name="mitigation"></a>Mitigación

Hay varias cosas que los usuarios pueden hacer para dar cabida a estos cambios:

-   Se pide a los usuarios contextualmente que elijan una aplicación predeterminada para controlar los tipos de archivo, los esquemas uri o ambos cuando no se haya especificado uno.
-   Los usuarios tienen la opción de cambiar su controlador predeterminado después de instalar nuevas aplicaciones que pueden controlar un tipo de archivo o un esquema de URI.
-   El panel de control de programas predeterminado permite a los usuarios establecer valores predeterminados para una aplicación, para un tipo de archivo, un esquema de URI o ambos; las aplicaciones pueden vincularse al panel de control
-   Los valores predeterminados se pueden cambiar desde Windows Explorer

## <a name="solution"></a>Solución

Como resultado de estos cambios, se proporciona esta guía de API:

-   La funcionalidad de algunas llamadas a métodos dentro de la API [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) ha cambiado y ya no se debe usar.

    -   **No llame** a [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) para determinar si una aplicación es el valor predeterminado.
    -   **No llame** a [QueryCurrentDefault para](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) determinar qué aplicación (si existe) es el valor predeterminado actual.
    -   **No llame** a [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll para](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) establecer la aplicación predeterminada.

-   Las instrucciones que se van a seguir son:

    -   **No realice consultas** para ver qué aplicación es el controlador predeterminado para los tipos de archivo o los esquemas uri.

    -   **No intente** supervisar los cambios en el controlador predeterminado para tipos de archivo o esquemas URI

    -   **No intente** establecer una aplicación como controlador predeterminado para tipos de archivo o esquemas URI

    -   **No intente** administrar los valores predeterminados para tipos de archivo o esquemas URI desde dentro de una aplicación

    -   **Realice** la integración con el panel de [control](../shell/default-programs.md) Establecer programas predeterminados si desea permitir que los usuarios de la aplicación accedan a la interfaz de usuario de administración predeterminada (ya no se admite la interfaz de usuario de administración dentro de la aplicación).

        -   Llamar [a IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) permite al usuario acceder a la página del panel de control["Establecer](../shell/default-programs.md)programas predeterminados" para la aplicación especificada.

## <a name="tests"></a>Pruebas

-   Prueba para comprobar que las aplicaciones se registran correctamente en el panel de control Establecer programas predeterminados
-   Pruebe para comprobar que las aplicaciones se registran correctamente para que aparezcan en la lista OpenWith de los tipos de archivo, esquemas URI o ambos, que se registran para controlar.
-   Pruebe para comprobar que aparecen nuevas notificaciones de aplicación después de instalar la aplicación y el usuario invoca un tipo de archivo, un esquema de URI o ambos, que la aplicación se ha registrado para controlar.

## <a name="resources"></a>Recursos

-   [Procedimientos recomendados para asociaciones de tipo de archivo y URI en Windows 8 Desktop Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))
-   [Asociaciones de tipo de archivo y presentación de la conferencia de compilación de Reproducción automática](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 