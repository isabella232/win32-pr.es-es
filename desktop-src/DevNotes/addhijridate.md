---
description: '\\Panel de control HKCU \\ internacional.'
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: AddHijriDate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907070"
---
# <a name="addhijridate"></a>AddHijriDate

**\\Panel de control HKCU \\ internacional**



| Tipo de datos | Intervalo                      | Valor predeterminado |
|-----------|----------------------------|---------------|
| Registro \_ SZ   | *Un valor de ajuste válido* | (Ninguna)        |



 

## <a name="description"></a>Descripción

Especifica ajustes en la fecha en el calendario Hijri.

El calendario Hijri es un calendario lunar utilizado en el mundo islámico. Los meses empiezan y terminan según un decreto que se basa en la observación de la nueva luna. Es difícil predecir con precisión el comienzo y el final de los meses, y hay variaciones regionales, por lo que se realiza un ajuste entre cero y dos días en el calendario.

El valor del registro **AddHijriDate** almacena este valor de ajuste como se indica a continuación.



| Value          | Significado                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddHijriDate-2 | Reste dos días.                                                                                                                                                                                                                    |
| AddHijriDate   | Reste un día.                                                                                                                                                                                                                     |
| (en blanco)        | No es necesario realizar ningún ajuste. (Si no se ha ajustado la fecha, esta entrada no aparece en el registro. Si la fecha se ha ajustado y se ha restaurado a su valor original, esta entrada aparece en el registro sin valor). |
| AddHijriDate + 1 | Agregue un día.                                                                                                                                                                                                                          |
| AddHijriDate + 2 | Agregue dos días.                                                                                                                                                                                                                         |



 

Esta entrada no existe en el registro de forma predeterminada. Puede agregarlo mediante el editor del registro Regedit.exe o mediante el método de cambio que se describe a continuación.

## <a name="change-method"></a>Cambiar método

Para cambiar el valor de esta entrada, o para agregarla al registro, primero Instale los archivos para los idiomas de escritura compleja y de derecha a izquierda. En el panel de control, haga clic en **configuración regional y de idioma y**, a continuación, haga clic en la pestaña **idiomas** . En **compatibilidad con idioma adicional**, active la casilla para **instalar archivos de idiomas de escritura compleja y de derecha a izquierda (incluido el tailandés)**. Haga clic en **OK**.

Para cambiar el valor de esta entrada o para agregarla al registro, en el panel de control, haga clic en **Opciones regionales y de idioma**. En el campo **estándares y formatos** , seleccione una configuración regional que use el calendario Hijri. Haga clic en el botón **personalizar** y, a continuación, haga clic en la pestaña **fecha** . En la lista desplegable **Ajustar fecha Hijri a:** , seleccione el valor adecuado. Haga clic en **Aceptar** y en **Aceptar** de nuevo.

## <a name="activation-method"></a>Método de activación

Los cambios que se realicen en esta entrada a través del panel de control surtirán efecto inmediatamente.

 

 



