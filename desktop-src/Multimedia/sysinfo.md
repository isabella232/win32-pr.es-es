---
title: sysinfo (comando)
description: El comando sysinfo recupera información del sistema MCI. El comando sysinfo es un comando del sistema MCI; lo interpreta directamente MCI.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- comando de sysinfo Windows multimedia
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666075"
---
# <a name="sysinfo-command"></a>sysinfo (comando)

El comando sysinfo recupera información del sistema MCI. El comando sysinfo es un comando del sistema MCI; lo interpreta directamente MCI.

Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.

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

Identificador de un dispositivo MCI o de un tipo de dispositivo. Si se especifica un tipo de dispositivo, debe ser un nombre de tipo de dispositivo MCI estándar, tal y como se muestra en el material de referencia del comando [**Capability**](capability.md) . Puede especificar "All" cuando la marca especificada en *lpszRequest* permite esa posibilidad.

</dd> <dt>

*lpszRequest* 
</dt> <dd>

Una de las marcas siguientes.



| Value                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <dt>**installname**</dt> </dl>               | Devuelve el nombre que aparece en el registro o el archivo de SYSTEM.INI que se usa para instalar el dispositivo abierto con el identificador de dispositivo especificado.<br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <dt>**volumen**</dt> </dl>                        | Devuelve el número de dispositivos MCI que aparecen en el registro o el archivo SYSTEM.INI del tipo especificado en el parámetro *lpszDeviceID* . Este identificador de dispositivo debe ser un nombre de tipo de dispositivo MCI estándar. Se omite cualquier dígito después del tipo de dispositivo. Si se especifica "All" para *lpszDeviceID* , se devuelve el número total de dispositivos MCI en el sistema.<br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <dt>**cantidad abierta**</dt> </dl>         | Devuelve el número de dispositivos MCI abiertos del tipo especificado en *lpszDeviceID*. Este identificador de dispositivo debe ser un nombre de tipo de dispositivo MCI estándar. Si se especifica "All" para *lpszDeviceID* , se devuelve el número total de dispositivos MCI abiertos en el sistema.<br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <dt>* * Nombre * Índice * * *</dt> </dl>                | Devuelve el nombre de un dispositivo MCI. El identificador de dispositivo debe ser un nombre de tipo de dispositivo MCI estándar. El *Índice* va de 1 al número de dispositivos de ese tipo. Si se especifica "All" para *lpszDeviceID*, *index* va de 1 al número total de dispositivos del sistema.<br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <dt>**nombre del *Índice* abierto**</dt> </dl> | Devuelve el nombre de un dispositivo MCI abierto. El identificador de dispositivo debe ser un nombre de tipo de dispositivo MCI estándar. El *Índice* va de 1 al número de dispositivos abiertos de ese tipo de dispositivo. Si se especifica "All" para *lpszDeviceID*, *index* va de 1 al número total de dispositivos abiertos en el sistema.<br/>                                          |



 

</dd> <dt>

*lpszFlags* 
</dt> <dd>

Puede ser "Wait", "Notify" o ambos. En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba". Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="examples"></a>Ejemplos

El siguiente comando devuelve el número de dispositivos de audio de onda de onda abiertos.

``` syntax
sysinfo waveaudio quantity open
```

El siguiente comando devuelve el nombre (alias de dispositivo) del primer dispositivo de audio de onda abierto.

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

[Cadenas de comandos MCI](mci-command-strings.md)
</dt> <dt>

[**pueda**](capability.md)
</dt> </dl>

 

