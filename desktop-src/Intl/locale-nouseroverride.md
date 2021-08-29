---
description: CONFIGURACIÓN REGIONAL \_ NOUSEROVERRIDE
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e80110c77c1834af80212673d59f9cd4d439ff9e81c3587d26845d1d91b16f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147378"
---
# <a name="locale_nouseroverride"></a>CONFIGURACIÓN REGIONAL \_ NOUSEROVERRIDE

> [!Caution]  
> Puesto que LOCALE \_ NOUSEROVERRIDE deshabilita las preferencias del usuario, se desaconseja su uso. Esta constante no garantiza [](custom-locales.md)la estabilidad de los datos, ya que las configuraciones regionales personalizadas, las actualizaciones del servicio, las distintas versiones del sistema operativo y otros escenarios pueden cambiar los datos de maneras inesperadas. Para obtener más información, vea [Using Persistent Locale Data](using-persistent-locale-data.md).

 

No hay invalidación de usuario. En varias funciones, por ejemplo, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) y [**GetLocaleInfoEx,**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)esta constante hace que la función omita cualquier invalidación de usuario y use el valor predeterminado del sistema para cualquier otra constante especificada en la llamada de función. La información se recupera de la base de datos de configuración regional, incluso si el identificador indica la configuración regional actual y el usuario ha cambiado algunos de los valores mediante el Panel de control, o si una aplicación ha cambiado estos valores mediante [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Si no se especifica esta constante, los valores que el usuario haya configurado desde el Panel de control o que una aplicación haya configurado mediante [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) tendrán prioridad sobre los valores de base de datos para la configuración regional predeterminada del sistema actual.

 

 



