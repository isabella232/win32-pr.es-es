---
title: Propiedad currentPositionTimecode de IWMPControls3
description: La propiedad currentPositionTimecode obtiene o establece la posición actual en el elemento multimedia actual con un formato de código de hora. Esta propiedad admite actualmente código de hora SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- Propiedad currentPositionTimecode Reproductor de Windows Media
- Propiedad currentPositionTimecode Reproductor de Windows Media , interfaz IWMPControls3
- Interfaz IWMPControls3 Reproductor de Windows Media , propiedad currentPositionTimecode
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070742"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a>Propiedad IWMPControls3::currentPositionTimecode

La **propiedad currentPositionTimecode** obtiene o establece la posición actual en el elemento multimedia actual con un formato de código de hora. Esta propiedad admite actualmente código de hora SMPTE.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es el código de hora de SMPTE.

## <a name="remarks"></a>Observaciones

El código de tiempo SMPTE proporciona una manera estándar de identificar un fotograma de vídeo individual, que es útil para sincronizar la reproducción. Si un archivo multimedia digital admite código de tiempo SMPTE, Reproductor de Windows Media recuperar la información de posición del código de hora actual o buscar en un fotograma de vídeo identificado por un código de hora determinado.

El código de tiempo de SMPTE identifica un fotograma determinado por el número de horas, minutos, segundos y fotogramas que lo separan de un marco de referencia determinado que el fotograma designa como tiempo cero. Normalmente, el período de tiempo cero es el inicio del archivo y un valor de código de tiempo de SMPTE determinado representa el tiempo transcurrido desde el inicio del archivo.

El código de hora está en el intervalo \[ *de formato* \] *hh*:*mm*:*ss*.*ff,* \[ *donde range* \] representa el intervalo, hh representa horas, *mm* representa minutos, *ss* representa segundos y *ff* representa fotogramas. Al establecer un valor para **currentPositionTimecode**, debe incluir los ocho dígitos, usando ceros como marcadores de posición.

\[*range* \] corresponde al miembro **wRange** de la estructura de datos Windows formato multimedia **WMT \_ TIMECODE \_ EXTENSION. \_** Para obtener más información sobre los intervalos de código de tiempo, consulte el SDK Windows Media Format.

La configuración y **obtención de currentPositionTimecode** solo se admite para los archivos que contienen información de código de tiempo de SMPTE.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **especifica currentPositionTimecode** como 1 hora, cero minutos, 30 segundos y 5 fotogramas. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


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
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls3 (VB y C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





