---
title: El IME de chino simplificado no admite las API del administrador de métodos de entrada
description: El IME de chino simplificado no admite las API del administrador de métodos de entrada
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149404"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>El IME de chino simplificado no admite las API del administrador de métodos de entrada

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

Las siguientes API del administrador de métodos de entrada no son compatibles con los IME de chino simplificado en Windows 8.1:

-   Interfaz IFECommon
-   Interfaz IFEDictionary
-   Interfaz IFELanguage
-   Interfaz IImePad
-   Interfaz IImePadApplet
-   Interfaz IImeSpecifyApplets

## <a name="manifestations"></a>Manifestaciones

Las funciones que usan esas API no funcionan con el IME de chino simplificado.

## <a name="solution"></a>Solución

Las aplicaciones deben diseñarse para que los usuarios puedan completar la tarea deseada sin usar la API especificada.

## <a name="resources"></a>Recursos

-   [Interfaces del administrador de métodos de entrada](../intl/input-method-manager-interfaces.md)
-   [IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interfaz IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interfaz IFEDictionary](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [IFELanguage](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [IImePad](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [IImePadApplet](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [IimePlugInDictDictionaryList](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [IImeSpecifyApplets](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 