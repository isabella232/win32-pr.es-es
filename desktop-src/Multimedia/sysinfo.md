---
title: Comando sysinfo
description: El comando sysinfo recupera la información del sistema de MCI. El comando sysinfo es un comando del sistema MCI; MCI la interpreta directamente.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- Comando sysinfo Windows Multimedia
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370262"
---
# <a name="sysinfo-command"></a>Comando sysinfo

El comando sysinfo recupera la información del sistema de MCI. El comando sysinfo es un comando del sistema MCI; MCI la interpreta directamente.

Para enviar este comando, llame a la [**función mciSendString**](/previous-versions//dd757161(v=vs.85)) con el *parámetro lpszCommand* establecido como se muestra a continuación.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszDeviceID* 
</dt> <dd>

Identificador de un tipo de dispositivo o dispositivo MCI. Si se especifica un tipo de dispositivo, debe ser un nombre de tipo de dispositivo MCI estándar, como se muestra en el material de referencia del [**comando de funcionalidad.**](capability.md) Puede especificar "all" cuando la marca especificada en *lpszRequest* permita esa posibilidad.

</dd> <dt>

*lpszRequest* 
</dt> <dd>

Una de las marcas siguientes.



| Value                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <dt>**installname**</dt> </dl>               | Devuelve el nombre que aparece en el registro o en SYSTEM.INI archivo usado para instalar el dispositivo abierto con el identificador de dispositivo especificado.<br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <dt>**quantity**</dt> </dl>                        | Devuelve el número de dispositivos MCI enumerados en el registro o el archivo SYSTEM.INI del tipo especificado en el *parámetro lpszDeviceID.* Este identificador de dispositivo debe ser un nombre de tipo de dispositivo MCI estándar. Se omiten todos los dígitos después del tipo de dispositivo. Si se especifica "all" para *lpszDeviceID,* se devuelve el número total de dispositivos MCI del sistema.<br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <dt>**quantity open**</dt> </dl>         | Devuelve el número de dispositivos MCI abiertos del tipo especificado en *lpszDeviceID.* Este identificador de dispositivo debe ser un nombre de tipo de dispositivo MCI estándar. Si se especifica "all" para *lpszDeviceID,* se devuelve el número total de dispositivos MCI abiertos en el sistema.<br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <dt>**name *index**</dt> </dl>                | Devuelve el nombre de un dispositivo MCI. El identificador del dispositivo debe ser un nombre de tipo de dispositivo MCI estándar. El *índice* oscila entre 1 y el número de dispositivos de ese tipo. Si se especifica "all" para *lpszDeviceID,* *el* índice oscila entre 1 y el número total de dispositivos del sistema.<br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <dt>**índice *de nombre* abierto**</dt> </dl> | Devuelve el nombre de un dispositivo MCI abierto. El identificador del dispositivo debe ser un nombre de tipo de dispositivo MCI estándar. El *índice* oscila entre 1 y el número de dispositivos abiertos de ese tipo de dispositivo. Si se especifica "all" para *lpszDeviceID,* *el* índice oscila entre 1 y el número total de dispositivos abiertos en el sistema.<br/>                                          |



 

</dd> <dt>

*lpszFlags* 
</dt> <dd>

Puede ser "wait", "notify" o ambos. En el caso de los dispositivos de vídeo digital y VCR, también se puede especificar "prueba". Para obtener más información sobre estas marcas, vea [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="examples"></a>Ejemplos

El comando siguiente devuelve el número de dispositivos de audio de forma de onda abiertos.

``` syntax
sysinfo waveaudio quantity open
```

El comando siguiente devuelve el nombre (alias de dispositivo) del primer dispositivo de audio de forma de onda abierto.

``` syntax
sysinfo waveaudio name 1 open
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadenas de comandos de MCI](mci-command-strings.md)
</dt> <dt>

[**Capacidad**](capability.md)
</dt> </dl>

 

