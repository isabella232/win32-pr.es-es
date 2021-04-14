---
title: Símbolos
description: En esta sección se describen las intercalaciones que parpadean en líneas, bloques o mapas de bits en el área de cliente de una ventana.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- recursos, insumos
- insumos, acerca de
- líneas intermitentes
- bloques en parpadeo
- parpadeo de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104424095"
---
# <a name="carets"></a>Símbolos

Un *símbolo de intercalación* es una línea, un bloque o un mapa de bits intermitentes en el área de cliente de una ventana. El símbolo de intercalación suele indicar el lugar en el que se insertará el texto o los gráficos.

En la ilustración siguiente se muestran algunas variaciones comunes en la apariencia del símbolo de intercalación.

![Muestra 5 formas diferentes que puede aparecer un símbolo de intercalación.](images/cscrt-01.png)

Las aplicaciones pueden crear un símbolo de intercalación, cambiar su tiempo de intermitencia y mostrar, ocultar o reubicar el símbolo de intercalación.

### <a name="in-this-section"></a>En esta sección



| Nombre                                   | Descripción                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [Acerca de las intercalaciones](about-carets.md)       | Describe las intercalaciones.<br/>                                              |
| [Usar las intercalaciones](using-carets.md)       | Ejemplos de código que muestran cómo realizar tareas relacionadas con las intercalaciones.<br/> |
| [Referencia de símbolo de intercalación](caret-reference.md) | Contiene la referencia de la API.<br/>                                    |



 

### <a name="caret-functions"></a>Funciones de símbolo de intercalación



| Nombre                                           | Descripción                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | Crea una nueva forma para el símbolo de intercalación del sistema y asigna la propiedad del símbolo de intercalación a la ventana especificada. La forma del símbolo de intercalación puede ser una línea, un bloque o un mapa de bits. <br/>                                                                                         |
| [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | Destruye la forma actual del símbolo de intercalación, libera el símbolo de intercalación de la ventana y quita el símbolo de intercalación de la pantalla. <br/>                                                                                                                                       |
| [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | Recupera el tiempo necesario para invertir los píxeles del símbolo de intercalación. El usuario puede establecer este valor. <br/>                                                                                                                                                            |
| [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | Copia la posición del símbolo de intercalación en la estructura de [**puntos**](/previous-versions//dd162805(v=vs.85)) especificada. <br/>                                                                                                                                                                    |
| [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | Quita el símbolo de intercalación de la pantalla. Ocultar un símbolo de intercalación no destruye su forma actual ni invalida el punto de inserción. <br/>                                                                                                                           |
| [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | Establece el tiempo de parpadeo del símbolo de intercalación en el número de milisegundos especificado. El tiempo de intermitencia es el tiempo transcurrido, en milisegundos, necesario para invertir los píxeles del símbolo de intercalación. <br/>                                                                                    |
| [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | Mueve el símbolo de intercalación a las coordenadas especificadas. Si la ventana que posee el símbolo de intercalación se creó con el estilo de clase **CS \_ OWNDC** , las coordenadas especificadas están sujetas al modo de asignación del contexto de dispositivo asociado a esa ventana. <br/> |
| [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | Hace que el símbolo de intercalación esté visible en la pantalla en la posición actual del símbolo de intercalación. Cuando el símbolo de intercalación se vuelve visible, comienza a parpadear automáticamente. <br/>                                                                                                          |



 

 

