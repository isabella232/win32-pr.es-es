---
title: Propiedad currentPositionTimecode de IWMPControls3
description: La propiedad currentPositionTimecode obtiene o establece la posición actual en el elemento multimedia actual mediante un formato de código de tiempo. Esta propiedad admite actualmente código de tiempo SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- propiedades de currentPositionTimecode Media Player de Windows
- propiedad currentPositionTimecode de Windows Media Player, interfaz IWMPControls3
- Interfaz IWMPControls3 Windows Media Player, propiedad currentPositionTimecode
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650140"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>IWMPControls3:: currentPositionTimecode (propiedad)

La propiedad **currentPositionTimecode** obtiene o establece la posición actual en el elemento multimedia actual mediante un formato de código de tiempo. Esta propiedad admite actualmente código de tiempo SMPTE.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System. String** que es el código de tiempo de SMPTE.

## <a name="remarks"></a>Observaciones

El código de tiempo SMPTE proporciona una forma estándar de identificar un fotograma de vídeo individual, que es útil para sincronizar la reproducción. Si un archivo multimedia digital admite código de tiempo SMPTE, Windows Media Player puede recuperar la información de posición del código de tiempo actual o buscar un fotograma de vídeo identificado por un código de tiempo determinado.

El código de tiempo SMPTE identifica un fotograma determinado por el número de horas, minutos, segundos y fotogramas que lo separan de un marco de referencia determinado, el marco designado como tiempo cero. Normalmente, el marco de cero de tiempo es el inicio del archivo y un valor de código de tiempo de SMPTE determinado representa el tiempo transcurrido desde el inicio del archivo.

El código de tiempo se encuentra en el intervalo de formato \[  \] *HH*:*mm*:*SS*.*FF* donde \[ *Range* \] representa el intervalo, HH representa las horas, *mm* representa los minutos, *SS* representa los segundos y *FF* representa los fotogramas. Al establecer un valor para **currentPositionTimecode**, debe incluir los ocho dígitos, usando ceros como marcadores de posición.

\[*intervalo* \] de corresponde al miembro **wRange** de la estructura de datos de **la \_ \_ extensión de \_ código de tiempo WMT** del formato de Windows Media. Para obtener más información acerca de los intervalos de código de tiempo, vea el SDK de Windows Media Format.

La configuración y la obtención de **currentPositionTimecode** solo se admiten para los archivos que contienen información de código de tiempo SMPTE.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se especifica **currentPositionTimecode** como 1 hora, cero minutos, 30 segundos y 5 fotogramas. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls3 (VB y C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





