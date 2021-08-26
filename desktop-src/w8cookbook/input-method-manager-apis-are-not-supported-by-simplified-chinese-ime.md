---
title: Las API del administrador de métodos de entrada no son compatibles con IME chino simplificado
description: Las API del administrador de métodos de entrada no son compatibles con IME chino simplificado
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0454df8df722992e321fd7fc6bd745382ea215116b2fd5a7797f2032a9c7e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935415"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>Las API del administrador de métodos de entrada no son compatibles con IME chino simplificado

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8.1  
Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

Las SIGUIENTES API del administrador de métodos de entrada no son compatibles con los IME de chino simplificado en Windows 8.1:

-   Interfaz IFECommon
-   Interfaz IFEDictionary
-   Interfaz IFELanguage
-   Interfaz de IImePad
-   Interfaz IImePadApplet
-   Interfaz IImeSpecifyApplets

## <a name="manifestations"></a>Manifestaciones

Las funciones que usan esas API no funcionan con IME chino simplificado.

## <a name="solution"></a>Solución

Las aplicaciones deben diseñarse para que los usuarios puedan completar la tarea deseada sin usar la API especificada.

## <a name="resources"></a>Recursos

-   [Interfaces del Administrador de métodos de entrada](../intl/input-method-manager-interfaces.md)
-   [IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interfaz IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interfaz IFEDictionary](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [IFELanguage](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [IImePad](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [IImePadApplet](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [IimePlugInDictDictionaryList](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [IImeSpecifyApplets](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 