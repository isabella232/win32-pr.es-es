---
title: Consideraciones de seguridad De Microsoft Windows Controles
description: En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con Windows controles.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167034"
---
# <a name="security-considerations-microsoft-windows-controls"></a>Consideraciones de seguridad: Controles de Windows Microsoft

En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con Windows controles. La información de este tema no proporciona todo lo que necesita saber sobre los problemas de seguridad: úsela como punto de partida y referencia para esta área tecnológica.

La interconectividad entre equipos es común; el principal problema de un desarrollador debe ser la seguridad de las aplicaciones. En las secciones siguientes se de abordan algunos posibles problemas de seguridad que se deben tener en cuenta al programar Windows controles.

-   [Mensajes de control terminados en NULL](#null-terminated-control-messages)
-   [Uso de cadenas](#string-use)
-   [Validación de entrada](#input-validation)
-   [Uso de contraseña](#password-use)
-   [alertas de seguridad](#security-alerts)
-   [Temas relacionados](#related-topics)

## <a name="null-terminated-control-messages"></a>Mensajes de control terminados en NULL

Muchos de los mensajes de control y macros tienen parámetros de cadena. A menudo, estos mensajes no validan las cadenas de entrada, en particular, no comprueban si hay una terminación `'\0'` . Al llamar a un mensaje que usa una cadena como parámetro, especifique explícitamente que la cadena termina en NULL.

## <a name="string-use"></a>Uso de cadenas

Al programar los Windows, es necesario manipular cadenas. Casi todos los controles requieren que se inserte texto. Por ejemplo, para rellenar un cuadro de lista debe cargar cadenas en el control . Dado que el uso incorrecto de cadenas suele provocar saturaciones de búfer, tome precauciones para evitar este riesgo de seguridad.

Para obtener más información sobre las saturaciones de búfer, vea *Escribir* código seguro de Michael Howard y David LeSeguridad, Microsoft Press, 2002 y Procedimientos recomendados para las [API de seguridad.](/windows/desktop/SecBP/best-practices-for-the-security-apis)

## <a name="input-validation"></a>Validación de entrada

Los siguientes mensajes de control pueden presentar problemas de seguridad.

-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)
-   [**SB \_ GETTEXT**](sb-gettext.md)
-   [**SB \_ GETTIPTEXT**](sb-gettiptext.md)
-   [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
-   [**GETTEXT de TTM \_**](ttm-gettext.md)
-   [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)

Si el texto cambia entre la llamada para obtener la longitud del texto y el tiempo que se muestra o se usa, puede producirse una saturación del búfer. Para evitarlo, debe validar la cadena antes de usarlo. Además, los mensajes que recuperan texto, [**CB \_ GETLBTEXT,**](cb-getlbtext.md) [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)y [**TTM \_ GETTEXT**](ttm-gettext.md), no tienen ningún parámetro de tamaño de búfer que presente la posibilidad de una saturación del búfer.

Al usar [**CB \_ GETLBTEXT**](cb-getlbtext.md) o [**SB \_ GETTEXT**](sb-gettext.md), primero debe llamar a [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) o [**SB \_ GETTEXTLENGTH para**](sb-gettextlength.md) obtener el tamaño del búfer. Algunos de estos mensajes, [**TB \_ GETBUTTONTEXT,**](tb-getbuttontext.md) [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)y [**TVM \_ GETISEARCHSTRING,**](tvm-getisearchstring.md)se pueden llamar con un valor de parámetro **NULL** para obtener la longitud de la cadena antes de invocar el mensaje para recuperar la cadena.

Un mensaje al que debe prestar especial atención es el mensaje [**SB \_ GETTIPTEXT**](sb-gettiptext.md) de la barra de estado. Este mensaje no proporciona ninguna manera de consultar la longitud de la cadena que se va a recuperar.

## <a name="password-use"></a>Uso de contraseña

Si usa controles de edición protegidos con contraseña (estilo [**ES \_ PASSWORD),**](edit-control-styles.md) el búfer que contiene el texto recuperado debe establecerse en cero lo antes posible para evitar exponer la contraseña del usuario en memoria.

## <a name="security-alerts"></a>Alertas de seguridad

En la tabla siguiente se enumeran las características que, si se usan incorrectamente, pueden poner en peligro la seguridad de las aplicaciones. Los mensajes enumerados aquí no proporcionan un parámetro que especifique el tamaño del búfer.



| Característica                                               | Mitigación                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | Asegúrese de que el búfer utilizado por la función se puede escribir en y termina en NULL.                                                                     |
| [**CB \_ GETLBTEXT**](cb-getlbtext.md)                 | Llame [**a CB \_ GETLBTEXTLEN para**](cb-getlbtextlen.md) obtener el tamaño del búfer y, a continuación, llame a CB [**\_ GETLBTEXT para**](cb-getlbtext.md) recuperar la cadena. |
| [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md) | Llame al mensaje con un **valor de parámetro NULL** para obtener el tamaño del búfer y, a continuación, llame al mensaje una segunda vez para recuperar la cadena.             |
| [**SB \_ GETTEXT**](sb-gettext.md)                     | Llame [**a SB \_ GETTEXTLENGTH para**](sb-gettextlength.md) obtener el tamaño del búfer y, a continuación, llame a SB [**\_ GETTEXT**](sb-gettext.md) para recuperar la cadena.   |
| [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)         | Llame al mensaje con un **valor de parámetro NULL** para obtener el tamaño del búfer y, a continuación, llame al mensaje una segunda vez para recuperar la cadena.             |
| [**GETTEXT de TTM \_**](ttm-gettext.md)                   | Este mensaje no proporciona una manera de conocer o especificar el tamaño del búfer.                                                                  |
| [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md) | Llame al mensaje pasando un valor de parámetro **NULL** para obtener el tamaño del búfer y, a continuación, llame al mensaje una segunda vez para recuperar la cadena.       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Otros recursos**
</dt> <dt>

[Seguridad de Microsoft](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Seguridad](/windows/desktop/security)
</dt> <dt>

[Recursos de seguridad de TechNet](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[Procedimientos recomendados para las API de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 