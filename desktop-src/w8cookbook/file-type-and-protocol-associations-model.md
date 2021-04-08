---
title: Modelo de tipo de archivo y asociaciones URI
description: Modelo de tipo de archivo y asociaciones URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078506"
---
# <a name="file-type-and-uri-associations-model"></a>Modelo de tipo de archivo y asociaciones URI

## <a name="platforms"></a>Plataformas

 **Clientes** : Windows 8  
**Servidores** : Windows Server 2012  



## <a name="description"></a>Descripción

El tipo de archivo y el modelo de asociación URI han cambiado en Windows 8. Las aplicaciones ya no pueden establecerse mediante programación como el controlador predeterminado para un tipo de archivo o URI. En su lugar, ahora el usuario controla siempre cuál es el controlador predeterminado para un tipo de archivo o un esquema de URI.

## <a name="manifestation"></a>Manifestación

El modo en que se presenta este cambio al usuario depende de cómo esté diseñado la aplicación, por ejemplo:

-   Muchas aplicaciones comprueban si son las predeterminadas cada vez que se ejecutan y, si no es así, solicitan al usuario que las establezca como predeterminada. Sin embargo, dado que las aplicaciones ya no pueden consultar con precisión para determinar qué aplicación es el controlador predeterminado para un tipo de archivo o un esquema de URI, no funciona ninguna de estas operaciones.
-   Muchas aplicaciones tienen un cuadro de diálogo o un menú integrado o en su instalador que especifica los tipos de archivo para los que la aplicación debe servir como valor predeterminado. Sin embargo, dado que las aplicaciones ya no se pueden establecer mediante programación como el controlador predeterminado para un tipo de archivo o un esquema de URI, esto ya no funciona.

## <a name="mitigation"></a>Mitigación

Hay varias cosas que los usuarios pueden hacer para dar cabida a estos cambios:

-   A los usuarios se les pide contextualmente que elijan una aplicación predeterminada para administrar los tipos de archivo, esquemas de URI o ambos cuando no se ha especificado ninguno.
-   A los usuarios se les ofrece la opción de cambiar el controlador predeterminado después de instalar nuevas aplicaciones que pueden controlar un tipo de archivo o un esquema de URI.
-   El panel de control programas predeterminados permite a los usuarios establecer valores predeterminados para una aplicación o un tipo de archivo, un esquema de URI o ambos. las aplicaciones pueden vincularse al panel de control
-   Los valores predeterminados se pueden cambiar desde el explorador de Windows

## <a name="solution"></a>Solución

Como resultado de estos cambios, se proporciona esta guía de API:

-   La funcionalidad de algunas llamadas de método dentro de la API de [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) ha cambiado y ya no debe usarse.

    -   **No** llame a [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) para determinar si una aplicación es la predeterminada.
    -   **No** llame a [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) para determinar qué aplicación (si existe) es el valor predeterminado actual.
    -   **No** llame a [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) para establecer la aplicación predeterminada

-   Las instrucciones que se van a avanzar son:

    -   **No** consulta para ver qué aplicación es el controlador predeterminado para los tipos de archivos o esquemas de URI

    -   **No** intente supervisar los cambios en el controlador predeterminado para tipos de archivo o esquemas de URI

    -   **No** intente establecer una aplicación como controlador predeterminado para los tipos de archivos o esquemas de URI.

    -   **No** intente administrar los valores predeterminados para los tipos de archivos o esquemas de URI desde una aplicación

    -   **Realice** la integración con el panel de control [establecer programas predeterminados](../shell/default-programs.md) si quiere permitir que los usuarios de la aplicación ACCEDAn a la interfaz de usuario de administración predeterminada (ya no se admite la interfaz de usuario de administración dentro de la aplicación).

        -   La llamada a [IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) permite al usuario tener acceso a la página del panel de control "[establecer programas predeterminados](../shell/default-programs.md)" de la aplicación especificada.

## <a name="tests"></a>Pruebas

-   Prueba para comprobar que las aplicaciones se registran correctamente en el panel de control de establecer programas predeterminados
-   Prueba para comprobar que las aplicaciones se registran correctamente para que aparezcan en la lista OpenWith para los tipos de archivo, esquemas de URI o ambos, que se registran para controlar
-   Prueba para comprobar que las nuevas notificaciones de aplicación aparecen después de instalar la aplicación y que el usuario invoca un tipo de archivo, un esquema de URI o ambos, que la aplicación ha registrado para controlar

## <a name="resources"></a>Recursos

-   [Prácticas recomendadas para las asociaciones de tipo de archivo y URI en aplicaciones de escritorio de Windows 8](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))
-   [Presentación de las asociaciones de tipo de archivo y de generación automática](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 