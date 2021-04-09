---
title: Consideraciones de seguridad controles de Microsoft Windows
description: En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con los controles de Windows.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104149703"
---
# <a name="security-considerations-microsoft-windows-controls"></a>Consideraciones de seguridad: controles de Microsoft Windows

En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con los controles de Windows. La información de este tema no proporciona todo lo que necesita saber acerca de los problemas de seguridad: Úselo como punto de partida y referencia para esta área tecnológica.

La interconectividad entre equipos es común; la principal preocupación del desarrollador debe ser la seguridad de las aplicaciones. En las secciones siguientes se describen algunos posibles problemas de seguridad que se deben tener en cuenta al programar controles de Windows.

-   [Mensajes de control terminados en null](#null-terminated-control-messages)
-   [Uso de cadenas](#string-use)
-   [Validación de entrada](#input-validation)
-   [Uso de contraseñas](#password-use)
-   [alertas de seguridad](#security-alerts)
-   [Temas relacionados](#related-topics)

## <a name="null-terminated-control-messages"></a>Mensajes de control terminados en null

Muchos de los mensajes y macros de control tienen parámetros de cadena. A menudo, estos mensajes no validan las cadenas de entrada, en particular, no comprueban si hay una terminación `'\0'` . Cuando se llama a un mensaje que utiliza una cadena como parámetro, especifique explícitamente que la cadena termina en NULL.

## <a name="string-use"></a>Uso de cadenas

Cuando se programan controles de Windows, es necesario manipular cadenas. Casi todos los controles requieren que se inserte texto. Por ejemplo, para rellenar un cuadro de lista, debe cargar las cadenas en el control. Dado que el uso incorrecto de cadenas suele provocar saturaciones de búfer, tome precauciones para evitar este riesgo de seguridad.

Para obtener más información sobre las saturaciones del búfer, vea *escribir código seguro* de Michael Howard y David LeBlanc, Microsoft Press, 2002 y [prácticas recomendadas para las API de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis).

## <a name="input-validation"></a>Validación de entrada

Los siguientes mensajes de control pueden presentar problemas de seguridad.

-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**\_GETISEARCHSTRING LVM**](lvm-getisearchstring.md)
-   [**GETTEXT de SB \_**](sb-gettext.md)
-   [**SB \_ GETTIPTEXT**](sb-gettiptext.md)
-   [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
-   [**TTM \_ GETTEXT**](ttm-gettext.md)
-   [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)

Si el texto cambia entre la llamada para obtener la longitud del texto y la hora en que se muestra o se usa el texto, se puede producir una saturación del búfer. Para evitar esto, debe validar la cadena antes de usarla. Además, los mensajes que recuperan Text, [**CB \_ GETLBTEXT**](cb-getlbtext.md), [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)y [**TTM \_ GETTEXT**](ttm-gettext.md), no tienen ningún parámetro de tamaño de búfer que presente el potencial de una saturación del búfer.

Cuando use [**CB \_ GETLBTEXT**](cb-getlbtext.md) o [**SB \_ GETTEXT**](sb-gettext.md), primero debe llamar a [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) o [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obtener el tamaño del búfer. Algunos de estos mensajes, [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)y [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md), se pueden llamar con un valor de parámetro **null** para obtener la longitud de la cadena antes de invocar el mensaje para recuperar la cadena.

Un mensaje que debe prestar especial atención a es el mensaje de [**\_ GETTIPTEXT de SB**](sb-gettiptext.md) de la barra de estado. Este mensaje no proporciona ninguna manera de consultar la longitud de la cadena que se va a recuperar.

## <a name="password-use"></a>Uso de contraseñas

Si usa controles de edición protegidos con contraseña ([**es \_**](edit-control-styles.md) decir, el estilo de contraseña), el búfer que contiene el texto recuperado debe establecerse en cero lo antes posible para evitar exponer la contraseña del usuario en la memoria.

## <a name="security-alerts"></a>Alertas de seguridad

En la tabla siguiente se enumeran las características que, si se usan incorrectamente, pueden poner en peligro la seguridad de las aplicaciones. Los mensajes que se enumeran aquí no proporcionan un parámetro que especifique el tamaño del búfer.



| Característica                                               | Mitigación                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | Asegúrese de que se puede escribir en el búfer usado por la función y que está terminado en NULL.                                                                     |
| [**CB \_ GETLBTEXT**](cb-getlbtext.md)                 | Llame a [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) para obtener el tamaño del búfer y, a continuación, llame a [**CB \_ GETLBTEXT**](cb-getlbtext.md) para recuperar la cadena. |
| [**\_GETISEARCHSTRING LVM**](lvm-getisearchstring.md) | Llame al mensaje con un valor de parámetro **null** para obtener el tamaño del búfer y, a continuación, llame al mensaje una segunda vez para recuperar la cadena.             |
| [**GETTEXT de SB \_**](sb-gettext.md)                     | Llame a [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obtener el tamaño del búfer y, a continuación, llame a la [**\_ GETTEXT de SB**](sb-gettext.md) para recuperar la cadena.   |
| [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)         | Llame al mensaje con un valor de parámetro **null** para obtener el tamaño del búfer y, a continuación, llame al mensaje una segunda vez para recuperar la cadena.             |
| [**TTM \_ GETTEXT**](ttm-gettext.md)                   | Este mensaje no proporciona una manera de conocer o especificar el tamaño del búfer.                                                                  |
| [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md) | Llame al mensaje pasando un valor de parámetro **null** para obtener el tamaño del búfer y, a continuación, llame al mensaje una segunda vez para recuperar la cadena.       |



 

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

[Prácticas recomendadas para las API de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 