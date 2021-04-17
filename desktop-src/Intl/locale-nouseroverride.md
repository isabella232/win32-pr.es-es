---
description: configuración regional \_ NOUSEROVERRIDE
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28c2f59358bf71936e3a812c10e061d7a169387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652701"
---
# <a name="locale_nouseroverride"></a>configuración regional \_ NOUSEROVERRIDE

> [!Caution]  
> Dado que la configuración regional \_ NOUSEROVERRIDE deshabilita las preferencias del usuario, se desaconseja su uso. Esta constante no garantiza la estabilidad de los datos, ya que las [configuraciones regionales personalizadas](custom-locales.md), las actualizaciones del servicio, las distintas versiones del sistema operativo y otros escenarios pueden cambiar los datos de maneras inesperadas. Para obtener más información, consulte [uso de datos de configuración regional persistentes](using-persistent-locale-data.md).

 

No se invalida el usuario. En varias funciones, por ejemplo, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) y [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), esta constante hace que la función omita cualquier invalidación de usuario y use el valor predeterminado del sistema para cualquier otra constante especificada en la llamada de función. La información se recupera de la base de datos de configuración regional, incluso si el identificador indica la configuración regional actual y el usuario ha cambiado algunos de los valores mediante el panel de control, o si una aplicación ha cambiado estos valores mediante [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Si no se especifica esta constante, los valores que el usuario haya configurado desde el panel de control o que una aplicación haya configurado con [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) tienen prioridad sobre la configuración de la base de datos para la configuración regional predeterminada del sistema actual.

 

 



