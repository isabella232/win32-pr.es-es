---
description: Cómo devolver los registros del diario de cambios que cumplen los criterios especificados.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Recorrer un búfer de registros del diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9384316e38c23951849006efc259268a7bdf33df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667691"
---
# <a name="walking-a-buffer-of-change-journal-records"></a><span data-ttu-id="5fe29-103">Recorrer un búfer de registros del diario de cambios</span><span class="sxs-lookup"><span data-stu-id="5fe29-103">Walking a Buffer of Change Journal Records</span></span>

<span data-ttu-id="5fe29-104">Los códigos de control que devuelven los registros del diario de cambios del número de secuencia de actualización (USN), los datos de los USN [**\_ leer \_ \_ diario USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) y fsctl de la [**\_ \_ \_ enumeración**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), devuelven datos similares en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5fe29-104">The control codes that return update sequence number (USN) change journal records, [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), return similar data in the output buffer.</span></span> <span data-ttu-id="5fe29-105">Ambos devuelven un USN seguido de cero o más registros de diario de cambios, cada uno de ellos en una estructura de registro [**USN \_ \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**USN \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) .</span><span class="sxs-lookup"><span data-stu-id="5fe29-105">Both return a USN followed by zero or more change journal records, each in a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure.</span></span>

<span data-ttu-id="5fe29-106">El volumen de destino de las operaciones de USN debe ser ReFS o NTFS 3,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5fe29-106">The target volume for USN operations must be ReFS or NTFS 3.0 or later.</span></span> <span data-ttu-id="5fe29-107">Para obtener la versión NTFS de un volumen, abra un símbolo del sistema con derechos de acceso de administrador y ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="5fe29-107">To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:</span></span>

<span data-ttu-id="5fe29-108">**FSUtil.exe FSInfo ntfsinfo** \*X \*\* \* *:*</span><span class="sxs-lookup"><span data-stu-id="5fe29-108">**FSUtil.exe FSInfo NTFSInfo** *X\*\*\*:*\*</span></span>

<span data-ttu-id="5fe29-109">donde *X* es la letra de la unidad del volumen.</span><span class="sxs-lookup"><span data-stu-id="5fe29-109">where *X* is the drive letter of the volume.</span></span>

<span data-ttu-id="5fe29-110">En la lista siguiente se identifican las formas de obtener los registros del diario de cambios:</span><span class="sxs-lookup"><span data-stu-id="5fe29-110">The following list identifies ways to get change journal records:</span></span>

-   <span data-ttu-id="5fe29-111">Use [**los \_ \_ \_ datos USN enum de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) para obtener una lista (enumeración) de todos los registros del diario de cambios entre dos USN.</span><span class="sxs-lookup"><span data-stu-id="5fe29-111">Use [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) to get a listing (enumeration) of all change journal records between two USNs.</span></span>
-   <span data-ttu-id="5fe29-112">Use [**el \_ \_ \_ diario de lectura de USN de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) para ser más selectivo, como la selección de razones específicas para los cambios o la devolución cuando se cierra un archivo.</span><span class="sxs-lookup"><span data-stu-id="5fe29-112">Use [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) to be more selective, such as selecting specific reasons for changes or returning when a file is closed.</span></span>

> [!Note]  
> <span data-ttu-id="5fe29-113">Ambas operaciones devuelven solo el subconjunto de registros del diario de cambios que cumplen los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="5fe29-113">Both of these operations return only the subset of change journal records that meet the specified criteria.</span></span>

 

<span data-ttu-id="5fe29-114">El USN devuelto como primer elemento en el búfer de salida es el USN del siguiente número de registro que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5fe29-114">The USN returned as the first item in the output buffer is the USN of the next record number to be retrieved.</span></span> <span data-ttu-id="5fe29-115">Use este valor para seguir leyendo los registros del límite final hacia delante.</span><span class="sxs-lookup"><span data-stu-id="5fe29-115">Use this value to continue reading records from the end boundary forward.</span></span>

<span data-ttu-id="5fe29-116">El miembro **filename** del [**Registro \_ USN \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**el \_ registro USN \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contiene el nombre del archivo al que se aplica el registro en cuestión.</span><span class="sxs-lookup"><span data-stu-id="5fe29-116">The **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contains the name of the file to which the record in question applies.</span></span> <span data-ttu-id="5fe29-117">El nombre de archivo varía en longitud, por lo que el registro **USN \_ \_ V2** y el **\_ registro USN \_ V3** son estructuras de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="5fe29-117">The file name varies in length, so **USN\_RECORD\_V2** and **USN\_RECORD\_V3** are variable length structures.</span></span> <span data-ttu-id="5fe29-118">Su primer miembro, **RecordLength**, es la longitud de la estructura (incluido el nombre de archivo), en bytes.</span><span class="sxs-lookup"><span data-stu-id="5fe29-118">Their first member, **RecordLength**, is the length of the structure (including the file name), in bytes.</span></span>

<span data-ttu-id="5fe29-119">Cuando trabaje con el miembro de **nombre** de archivo de las estructuras de registro [**USN \_ \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) y [**\_ registro USN \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) , no suponga que el nombre de archivo contiene un \\ delimitador "0" final.</span><span class="sxs-lookup"><span data-stu-id="5fe29-119">When you work with the **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structures, do not assume that the file name contains a trailing '\\0' delimiter.</span></span> <span data-ttu-id="5fe29-120">Para determinar la longitud del nombre de archivo, use el miembro **FileNameLength** .</span><span class="sxs-lookup"><span data-stu-id="5fe29-120">To determine the length of the file name, use the **FileNameLength** member.</span></span>

<span data-ttu-id="5fe29-121">En el ejemplo siguiente se llama a [**FSCTL \_ leer el \_ \_ diario USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) y se recorre el búfer de los registros del diario de cambios que devuelve la operación.</span><span class="sxs-lookup"><span data-stu-id="5fe29-121">The following example calls [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and walks the buffer of change journal records that the operation returns.</span></span>


```C++
#include <Windows.h>
#include <WinIoCtl.h>
#include <stdio.h>

#define BUF_LEN 4096

void main()
{
   HANDLE hVol;
   CHAR Buffer[BUF_LEN];

   USN_JOURNAL_DATA JournalData;
   READ_USN_JOURNAL_DATA ReadData = {0, 0xFFFFFFFF, FALSE, 0, 0};
   PUSN_RECORD UsnRecord;  

   DWORD dwBytes;
   DWORD dwRetBytes;
   int I;

   hVol = CreateFile( TEXT("\\\\.\\c:"), 
               GENERIC_READ | GENERIC_WRITE, 
               FILE_SHARE_READ | FILE_SHARE_WRITE,
               NULL,
               OPEN_EXISTING,
               0,
               NULL);

   if( hVol == INVALID_HANDLE_VALUE )
   {
      printf("CreateFile failed (%d)\n", GetLastError());
      return;
   }

   if( !DeviceIoControl( hVol, 
          FSCTL_QUERY_USN_JOURNAL, 
          NULL,
          0,
          &JournalData,
          sizeof(JournalData),
          &dwBytes,
          NULL) )
   {
      printf( "Query journal failed (%d)\n", GetLastError());
      return;
   }

   ReadData.UsnJournalID = JournalData.UsnJournalID;

   printf( "Journal ID: %I64x\n", JournalData.UsnJournalID );
   printf( "FirstUsn: %I64x\n\n", JournalData.FirstUsn );

   for(I=0; I<=10; I++)
   {
      memset( Buffer, 0, BUF_LEN );

      if( !DeviceIoControl( hVol, 
            FSCTL_READ_USN_JOURNAL, 
            &ReadData,
            sizeof(ReadData),
            &Buffer,
            BUF_LEN,
            &dwBytes,
            NULL) )
      {
         printf( "Read journal failed (%d)\n", GetLastError());
         return;
      }

      dwRetBytes = dwBytes - sizeof(USN);

      // Find the first record
      UsnRecord = (PUSN_RECORD)(((PUCHAR)Buffer) + sizeof(USN));  

      printf( "****************************************\n");

      // This loop could go on for a long time, given the current buffer size.
      while( dwRetBytes > 0 )
      {
         printf( "USN: %I64x\n", UsnRecord->Usn );
         printf("File name: %.*S\n", 
                  UsnRecord->FileNameLength/2, 
                  UsnRecord->FileName );
         printf( "Reason: %x\n", UsnRecord->Reason );
         printf( "\n" );

         dwRetBytes -= UsnRecord->RecordLength;

         // Find the next record
         UsnRecord = (PUSN_RECORD)(((PCHAR)UsnRecord) + 
                  UsnRecord->RecordLength); 
      }
      // Update starting USN for next call
      ReadData.StartUsn = *(USN *)&Buffer; 
   }

   CloseHandle(hVol);

}
```



<span data-ttu-id="5fe29-122">El tamaño, en bytes, de cualquier registro especificado por una estructura de registro [**USN \_ \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o un [**\_ registro USN \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) es, como máximo, `((MaxComponentLength - 1) * Width) + Size` donde *MaxComponentLength* es la longitud máxima en caracteres del nombre del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="5fe29-122">The size in bytes of any record specified by a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure is at most `((MaxComponentLength - 1) * Width) + Size` where *MaxComponentLength* is the maximum length in characters of the record file name.</span></span> <span data-ttu-id="5fe29-123">El ancho es el tamaño de un carácter ancho *y el tamaño* de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5fe29-123">The width is the size of a wide character, and the *Size* is the size of the structure.</span></span>

<span data-ttu-id="5fe29-124">Para obtener la longitud máxima, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine el valor al que apunta el parámetro *lpMaximumComponentLength* .</span><span class="sxs-lookup"><span data-stu-id="5fe29-124">To obtain the maximum length, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the value pointed to by the *lpMaximumComponentLength* parameter.</span></span> <span data-ttu-id="5fe29-125">Reste uno de *MaxComponentLength* para que tenga en cuenta el hecho de que la definición del [**\_ registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) y el [**\_ registro USN \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) incluye un carácter del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="5fe29-125">Subtract one from *MaxComponentLength* to account for the fact that the definition of [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) includes one character of the file name.</span></span>

<span data-ttu-id="5fe29-126">En el lenguaje de programación C, el mayor tamaño de registro posible es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="5fe29-126">In the C programming language, the largest possible record size is the following:</span></span>

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
